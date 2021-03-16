<template>
    <div class="d-flex justify-content-center">
      <div id="todaycontainer" class=" d-flex flex-column bd-highlight mb-3 ">
        <div class="whiteColor flex-grow-1 bd-highlight border-justify">
          <div class =" current-temperature">{{APIdata.temp}}</div>
          <div class ="celsius-symbol">o</div>
          <div class = "current-weather">| {{APIdata.weatherType}}</div>
          <div>
            <img class ="current-weather-image-rectangle" alt="cloud logo" src ="../assets/Rectangle 11.png"/>
            <img class ="current-weather-image-ellipse" alt="cloud logo" src ="../assets/Ellipse 1.png"/>
          </div>
          <div class = "city-name">{{APIdata.city}}</div>
          <div class = "city-location">{{APIdata.country}}</div>
          <div class= "border-box"></div>
          <div class = "current-weather-info-container">
            <div class ="humidity-text">Humidity</div>
            <div class ="humidity-value">{{APIdata.humidity}}%</div>
            <div class ="UV-index-text">UV Index</div>
            <div class ="UV-index-value">11</div>
            <div class ="wind-text">Wind</div>
            <div class ="wind-value">{{APIdata.wind}}kmh</div>
          </div>
        </div>      
      </div>
    </div>
</template>

<script>
export default {
  name:"Today",
  props: ['APIdata'],
}
</script>

<style>

.whiteColor{
  background:white;
}

#todaycontainer{
  position: relative;
  width: 375px;
  height: 812px;
  background:white;
}
.header{
  height: 44px;
}
.footer{
  height:34px;
}
.border-justify{
  margin: 0 24px 0 24px;
}
.current-temperature{
  position: absolute;
  width: 52px;
  height: 44px;
  left: 24px;
  top: 143px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 42px;
  line-height: 44px;
  /* identical to box height, or 105% */
  color: #000000;
}
.celsius-symbol{
  position: absolute;
  width: 11px;
  height: 18px;
  left: 71px;
  top: 137px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 18px;
  /* identical to box height, or 112% */
  color: #000000;
}
.current-weather{
  /* | Party Cloudy */
  position: absolute;
  left: 22.93%;
  right: 50.93%;
  top: 19.21%;
  bottom: 78.33%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */
  color: #000000;
}
.current-weather-image-sun{
  /* Ellipse 1 */
  position: absolute;
  width: 49.23px;
  height: 49.23px;
  left: 267px;
  top: 123px;
  /* background: linear-gradient(180deg, #FFD800 0%, rgba(255, 107, 0, 0.64) 100%);  */
}
.current-weather-image-rectangle{
  /* Rectangle 11 */
position: absolute;
width: 65.64px;
height: 24.62px;
left: 281.36px;
top: 153.77px;
background: linear-gradient(180deg, #61BDFF 0%, #FFFFFF 100%);
border-radius: 100px;
}
.current-weather-image-ellipse{
  /* Ellipse 1 */
  position: absolute;
  width: 36.92px;
  height: 36.92px;
  left: 299.82px;
  top: 137.36px;
  background: linear-gradient(180deg, #61BDFF 0%, #FFFFFF 100%);
  border-radius: 100px;
}
.city-name{
  position: absolute;
  /* width: 135px; */
  height: 26px;
  /* left: 24px; */
  top: 221px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 26px;
  /* identical to box height, or 130% */
  color: #000000;
}
.city-location{
  /* South Jakarta, Indonesia */
  position: absolute;
  /* left: 6.4%; */
  /* right: 54.13%; */
  top: 31.4%;
  bottom: 66.13%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 20px;
  /* identical to box height, or 167% */
  text-align: center;
  color: #000000;
}
.current-weather-info-container{
  position: absolute;
  width: 327px;
  height: 80px;
  left: 0px;
  top: 313px;
}
.humidity-text{
  /* Humidity */
  position: absolute;
  left: 9.07%;
  right: 75.73%;
  top: 41.26%;
  bottom: 57.02%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  /* identical to box height, or 117% */
  text-align: center;
  color: #000000;
}
.humidity-value{
/* 61% */
  position: absolute;
  width: 30px;
  height: 26px;
  left: 42px;
  top: 8px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 26px;
  /* identical to box height, or 162% */
  text-align: center;
  color: #000000;
}
.UV-index-text{
  /* UV Index */
  position: absolute;
  left: 42.67%;
  right: 42.67%;
  top: 41.26%;
  bottom: 57.02%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  /* identical to box height, or 117% */
  text-align: center;
  color: #000000;
}
.UV-index-value{
  /* 11 */
  position: absolute;
  width: 13px;
  height: 26px;
  left: 156px;
  top: 8px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 26px;
  /* identical to box height, or 162% */
  text-align: center;
  color: #000000;
}
.wind-text{
  /* Wind */
  position: absolute;
  left: 78.93%;
  right: 12.27%;
  top: 41.26%;
  bottom: 57.02%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  /* identical to box height, or 117% */
  text-align: center;
  color: #000000;
}
.wind-value{
  /* E 8 kmh */
  position: absolute;
  width: 68px;
  height: 26px;
  left: 239px;
  top: 8px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 26px;
  /* identical to box height, or 162% */
  text-align: center;
  color: #000000;
}
.border-box{
  position: absolute;
  width: 267px;
  height: 56px;
  left: 30px;
  top: 337px;
  }
</style>
