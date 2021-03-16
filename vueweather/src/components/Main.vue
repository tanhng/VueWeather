<template>
  <div >
    <Today :APIdata='APIdata'/>
    <NextDays :APIdata='APIdata'/>
  </div>
</template>

<script>
import Today from "./Today";
import NextDays from "./NextDays";
import axios from "axios";
export default {
  components: {
    Today, 
    NextDays 
    },
  data(){
    return{
      APIdata:{
          temp:null,
          weatherType:null,
          city:null,
          country:null,
          humidity:null,
          wind:null,
          UV:null,
      }
    }
  },
  beforeCreate(){
    axios
      .get('https://api.openweathermap.org/data/2.5/weather?q=Hanoi&appid=4595c76aec5bf5973b34ac4e95b287c5')
      .then(response => {
          this.APIdata.temp=Math.ceil(response.data.main.temp-271.15);
          this.APIdata.weatherType=response.data.weather[0].main;
          this.APIdata.city=response.data.name;
          this.APIdata.country=response.data.sys.country;
          this.APIdata.wind=response.data.wind.speed;
          this.APIdata.humidity=response.data.main.humidity;
      })
  }
};
</script>
<style>
</style>