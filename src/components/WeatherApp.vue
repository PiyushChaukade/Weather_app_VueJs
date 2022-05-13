<template>
<section>

  <div id="img"> 

  <div id="div1">  <font-awesome-icon icon="fa-solid fa-user-secret" />
     <img :src=URL />
      <h3>{{city_Name}} City</h3>
      <h1>{{temp}} ℃</h1>
<br>

  <span><input id="inputSearch" v-model="inputvalue" placeholder="Search Location" v-on:keyup.enter="getValue" >  </span>
  <span id="inside"><i @click="getValue" class="fa fa-search-location"></i></span>
  <!-- <button id="inputButton1" @click="getValue">Search</button> -->

  <br>
   <br>
      <span id="hovering"> <img src="../../icons/sunrise.png" />&nbsp;</span>
      <p class="sunset">{{sunrise}}</p>
      <br>
      <span id="hovering" > <img src="../../icons/sunset.png" /> &nbsp;</span>
      <p class="sunset">{{sunset}}</p>
      <br>
      <span  id="hovering"> <img class="calendar" src="../../icons/calendar.png" /> &nbsp;</span>
      <p class="currenttime">{{currentTime}}</p>


  </div>

  <div id="div2">

  <div id="div2_1">
   <span id="humidty"> <img src="../../icons/humidity.png" /> </span>
   <span id="humidty1" > Humidity</span>
   <p >{{humidity}} %</p>
  </div>

  <div id="div2_1">
   <span id="humidty"> <img src="../../icons/pressure.png" /> </span>
   <span id="humidty1" > Air Pressure</span>
   <p >{{air_pressure}} PS</p>
  </div>

  

   <div id="div2_1">
   <span id="humidty"> <img src="../../icons/raindrops.png" /> </span>
   <span id="humidty1" > Dew</span>
   <p >{{dew_point}} °C Td</p>
  </div>

 <div id="div2_1">
   <span id="humidty"> <img src="../../icons/wind.png" /> </span>
   <span id="humidty1" > Wind Speed</span>
   <p >{{windspeed}} km/h</p>
  </div>

   <div id="div2_1">
   <span id="humidty"> <img src="../../icons/magnifying-glass.png" /> </span>
   <span id="humidty1" > Visibility </span>
   <p >{{visibility}} km</p>
  </div>


  </div>
  <br>
     <div id="buttonChange">
  
    <button @click="prev">ᐊ</button>
    <button @click="showHourly">Hourly</button>
    <button @click="next">ᐅ</button>
    <button @click="showDaily">Daily</button>
   
    
    </div>

  <div id="div3" v-if="dataHourly" >

<div id="div3_1"> 
   <p>{{date1}}</p>
  <h1>{{date2}} ℃</h1>
  <p>Feels like {{date3}} ℃ </p>
   
  <p>   <img :src=URL1 /></p>

  </div>

  <div id="div3_1"> 
   <p>{{date5}}</p>
  <h1>{{date6}} ℃</h1>
  <p> Feels like {{date7}} ℃ </p>
   
  <p>   <img :src=URL2 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{date9}}</p>
  <h1>{{date10}} ℃</h1>
  <p>Feels like {{date11}} ℃ </p>
   
  <p>   <img :src=URL3 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{date13}}</p>
  <h1>{{date14}} ℃</h1>
  <p>Feels like {{date15}} ℃ </p>
   
  <p>   <img :src=URL4 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{date17}}</p>
  <h1>{{date18}} ℃</h1>
  <p>Feels like {{date19}} ℃ </p>
   
  <p>   <img :src=URL5 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{date21}}</p>
  <h1>{{date22}} ℃</h1>
  <p>Feels like {{date23}} ℃ </p>
   
  <p>   <img :src=URL6 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{date25}}</p>
  <h1>{{date26}} ℃</h1>
  <p>Feels like {{date27}} ℃ </p>
   
  <p>   <img :src=URL7 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{date29}}</p>
  <h1>{{date30}} ℃</h1>
  <p> Feels like {{date31}} ℃ </p>
   
  <p>   <img :src=URL8 /></p>

  </div>

  </div>


 <!-- daily data -->
 <div id="div3" v-else>

<div id="div3_1"> 
   <p>{{daily1}}</p>
  <h1>{{daily2}} ℃</h1>
  <p>Feels like {{daily3}} ℃</p>
   
  <p>   <img :src=URLD1 /></p>

  </div>

  <div id="div3_1"> 
   <p>{{daily5}}</p>
  <h1>{{daily6}} ℃</h1>
  <p>Feels like {{daily7}} ℃</p>
   
  <p>   <img :src=URLD2 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{daily9}}</p>
  <h1>{{daily10}} ℃</h1>
  <p>Feels like {{daily11}} ℃ </p>
   
  <p>   <img :src=URLD3 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{daily13}}</p>
  <h1>{{daily14}} ℃</h1>
  <p>Feels like {{daily15}} ℃ </p>
   
  <p>   <img :src=URLD4 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{daily17}}</p>
  <h1>{{daily18}} ℃</h1>
  <p>Feels like {{daily19}} ℃ </p>
   
  <p>   <img :src=URLD5 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{daily21}}</p>
  <h1>{{daily22}} ℃</h1>
  <p>Feels like {{daily23}} ℃ </p>
   
  <p>   <img :src=URLD6 /></p>

  </div>

   <div id="div3_1"> 
   <p>{{daily25}}</p>
  <h1>{{daily26}} ℃</h1>
  <p>Feels like {{daily27}} ℃ </p>
   
  <p>   <img :src=URLD7 /></p>

  </div>


   <div id="div3_1"> 
   <p>{{daily29}}</p>
  <h1>{{daily30}} ℃</h1>
  <p>Feels like {{daily31}} ℃ </p>
   
  <p><img :src=URLD8 /></p>

  </div>




  </div>

 

           
    
    <!-- <h1 >dew{{dew_point}}</h1> -->
    <!-- <h1 >hum{{humidity}}</h1> -->
    <!-- <h1 >pre{{air_pressure}}</h1> -->
    <!-- <h1 > sunrise{{sunrise}}</h1>
    <h1 >sunset{{sunset}}</h1>
    <h1 >visi{{visibility}}</h1> -->
    <!-- <h1 >date{{currentTime}}</h1> --> 
    <!-- <h1 >spped{{windspeed}}</h1> -->

    <!-- //<h1>{{icon}}</h1> -->
   <!-- // <img src=`http://openweathermap.org/img/wn/${{icon}}@4x.png`> -->
   

   

  </div>
  
</section>
 
</template>
<script>
  //import { library } from '@fortawesome/fontawesome-svg-core'
  //import { faUserSecret } from '@fortawesome/free-solid-svg-icons'
import axios from "axios"
//library.add(faUserSecret)
export default {
  
  data(){
    return{
       latitude:'',
       longitude:'',
       inputvalue:'',
       temp:'',
       dew_point:'',
       humidity:'',
       air_pressure:'',
       sunrise:'',
       sunset:'',
       visibility:'',
       currentTime:'',
       windspeed:'',

       city_Name:'',
       URL:'',

       date1:'',
       date2:'',
       date3:'',
       date4:'',
       URL1:'',
      i:0,
      j:1,
      k:2,
      l:3,
      m:4,
      n:5,
      o:6,
      p:7,

       date5:'',
       date6:'',
       date7:'',
       date8:'',
       URL2:'',

       date9:'',
       date10:'',
       date11:'',
       date12:'',
       URL3:'',

       date13:'',
       date14:'',
       date15:'',
       date16:'',
       URL4:'',

       date17:'',
       date18:'',
       date19:'',
       date20:'',
       URL5:'',

       date21:'',
       date22:'',
       date23:'',
       date24:'',
       URL6:'',

       date25:'',
       date26:'',
       date27:'',
       date28:'',
       URL7:'',

       date29:'',
       date30:'',
       date31:'',
       date32:'',
       URL8:'',



       daily1:'',
       daily2:'',
       daily3:'',
       daily4:'',
       URLD1:'',

       daily5:'',
       daily6:'',
       daily7:'',
       daily8:'',
       URLD2:'',

       daily9:'',
       daily10:'',
       daily11:'',
       daily12:'',
       URLD3:'',

       daily13:'',
       daily14:'',
       daily15:'',
       daily16:'',
       URLD4:'',

       daily17:'',
       daily18:'',
       daily19:'',
       daily20:'',
       URLD5:'',

       daily21:'',
       daily22:'',
       daily23:'',
       daily24:'',
       URLD6:'',

       daily25:'',
       daily26:'',
       daily27:'',
       daily28:'',
       URLD7:'',

       daily29:'',
       daily30:'',
       daily31:'',
       daily32:'',
       URLD8:'',


      dataHourly:true,
      dataDaily:false,
      nextclick:0,
      prevclick:0,

    

       //Enter values
       lat:'',
       long:'',
       saveDatalat:JSON.parse(localStorage.getItem("latitude")),
       saveDatalong:JSON.parse(localStorage.getItem("longitude")),



    }
  },
 
  methods:{
    
    findMyLocation(){
      if(this.saveDatalat==null || this.saveDatalong==null){
       // axios.get(`https://api.openweathermap.org/data/2.5/onecall?q=mumbai&appid=dad624d112b01d43844c2284c461e811`).then((res)=>console.log(res.data))
       if(navigator.geolocation){
         navigator.geolocation.getCurrentPosition(position=>{
           this.latitude=position.coords.latitude
           this.longitude=position.coords.longitude
           this.weather();
           this.cityName();



         },
         error=>{
           console.log(error.message)
         })
       }
      }else{


        axios.get(`https://api.openweathermap.org/data/2.5/weather?lat=${this.saveDatalat}&lon=${this.saveDatalong}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
      
       console.log(res.data)
      //  this.lat=res.data.coord.lat;
      //  this.long=res.data.coord.lon;

       this.city_Name=res.data.name;
      })


          axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.saveDatalat}&lon=${this.saveDatalong}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
       console.log(res.data)
        this.temp=Math.ceil((res.data.current.temp)-273);
        this.dew_point=res.data.current.dew_point;
        this.humidity=res.data.current.humidity;
        this.air_pressure=res.data.current.pressure;

        let sunriseTime=res.data.current.sunrise;
        let riseTime=new Date(sunriseTime*1000)
         this.sunrise=riseTime.toLocaleTimeString();


        let sunsetTime=res.data.current.sunset;
         let setTime=new Date(sunsetTime*1000)
         this.sunset=setTime.toLocaleTimeString();

        this.visibility=((res.data.current.visibility)/1000);
        
        let current_date=(res.data.current.dt);
        let time=new Date(current_date*1000)
         this.currentTime=time;

        this.windspeed=res.data.current.wind_speed;
        var icon=res.data.current.weather[0].icon;
        console.log(this.icon)
        var url=`http://openweathermap.org/img/w/${icon}.png`
        this.URL=url;

//hourly

      
        let hourly_date1=(res.data.hourly[0].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[0].temp)-273);
        this.date3=Math.ceil((res.data.hourly[0].feels_like)-273)
        this.date4=res.data.hourly[0].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;

//2
   
         let hourly_date2=(res.data.hourly[1].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[1].temp)-273);
        this.date7=Math.ceil((res.data.hourly[1].feels_like)-273)
        this.date8=res.data.hourly[1].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[2].dt);
        let D3=new Date(hourly_date3*1000);
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[2].temp)-273);
        this.date11=Math.ceil((res.data.hourly[2].feels_like)-273)
        this.date12=res.data.hourly[2].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[3].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[3].temp)-273);
        this.date15=Math.ceil((res.data.hourly[3].feels_like)-273)
        this.date16=res.data.hourly[3].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[4].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
         
        this.date18=Math.ceil((res.data.hourly[4].temp)-273);
        this.date19=Math.ceil((res.data.hourly[4].feels_like)-273)
        this.date20=res.data.hourly[4].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[5].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[5].temp)-273);
        this.date23=Math.ceil((res.data.hourly[5].feels_like)-273)
        this.date24=res.data.hourly[5].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[6].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
         
        this.date26=Math.ceil((res.data.hourly[6].temp)-273);
        this.date27=Math.ceil((res.data.hourly[6].feels_like)-273)
        this.date28=res.data.hourly[6].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[7].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[7].temp)-273);
        this.date31=Math.ceil((res.data.hourly[7].feels_like)-273)
        this.date32=res.data.hourly[6].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 


        
//daily

      //1
         let Daily_date1=(res.data.daily[0].dt);
        let day1=new Date(Daily_date1*1000);
        this.daily1=day1.toLocaleDateString()
         
        this.daily2=Math.ceil((res.data.daily[0].temp.day)-273);
        this.daily3=Math.ceil((res.data.daily[0].feels_like.day)-273);
        this.daily4=res.data.daily[0].weather[0].icon;

        var urld1=`http://openweathermap.org/img/w/${this.daily4}.png`
        this.URLD1=urld1;


        //2
        let Daily_date2=(res.data.daily[1].dt);
        let day2=new Date(Daily_date2*1000);
        this.daily5=day2.toLocaleDateString();
     
        this.daily6=Math.ceil((res.data.daily[1].temp.day)-273);
        this.daily7=Math.ceil((res.data.daily[1].feels_like.day)-273);
        this.daily8=res.data.daily[1].weather[0].icon;

        var urld2=`http://openweathermap.org/img/w/${this.daily8}.png`
        this.URLD2=urld2;

//3

        let Daily_date3=(res.data.daily[2].dt);
        let day3=new Date(Daily_date3*1000);
        this.daily9=day3.toLocaleDateString();
     
        this.daily10=Math.ceil((res.data.daily[2].temp.day)-273);
        this.daily11=Math.ceil((res.data.daily[2].feels_like.day)-273);
        this.daily12=res.data.daily[2].weather[0].icon;

        var urld3=`http://openweathermap.org/img/w/${this.daily12}.png`
        this.URLD3=urld3;

        //4
           let Daily_date4=(res.data.daily[3].dt);
        let day4=new Date(Daily_date4*1000);
        this.daily13=day4.toLocaleDateString();
     
        this.daily14=Math.ceil((res.data.daily[3].temp.day)-273);
        this.daily15=Math.ceil((res.data.daily[3].feels_like.day)-273);
        this.daily16=res.data.daily[3].weather[0].icon;

        var urld4=`http://openweathermap.org/img/w/${this.daily16}.png`
        this.URLD4=urld4;


//5
let Daily_date5=(res.data.daily[4].dt);
        let day5=new Date(Daily_date5*1000);
        this.daily17=day5.toLocaleDateString();
     
        this.daily18=Math.ceil((res.data.daily[4].temp.day)-273);
        this.daily19=Math.ceil((res.data.daily[4].feels_like.day)-273);
        this.daily20=res.data.daily[4].weather[0].icon;

        var urld5=`http://openweathermap.org/img/w/${this.daily20}.png`
        this.URLD5=urld5;

        //6
        let Daily_date6=(res.data.daily[5].dt);
        let day6=new Date(Daily_date6*1000);
        this.daily21=day6.toLocaleDateString();
     
        this.daily22=Math.ceil((res.data.daily[5].temp.day)-273);
        this.daily23=Math.ceil((res.data.daily[5].feels_like.day)-273);
        this.daily24=res.data.daily[5].weather[0].icon;

        var urld6=`http://openweathermap.org/img/w/${this.daily24}.png`
        this.URLD6=urld6;

        //7
        let Daily_date7=(res.data.daily[6].dt);
        let day7=new Date(Daily_date7*1000);
        this.daily25=day7.toLocaleDateString();
     
        this.daily26=Math.ceil((res.data.daily[6].temp.day)-273);
        this.daily27=Math.ceil((res.data.daily[6].feels_like.day)-273);
        this.daily28=res.data.daily[6].weather[0].icon;

        var urld7=`http://openweathermap.org/img/w/${this.daily28}.png`
        this.URLD7=urld7;

         //8

        let Daily_date8=(res.data.daily[7].dt);
        let day8=new Date(Daily_date8*1000);
        this.daily29=day8.toLocaleDateString();
     
        this.daily30=Math.ceil((res.data.daily[7].temp.day)-273);
        this.daily31=Math.ceil((res.data.daily[7].feels_like.day)-273);
        this.daily32=res.data.daily[7].weather[0].icon;

        var urld8=`http://openweathermap.org/img/w/${this.daily32}.png`
        this.URLD8=urld8;

      })
      }
    },
    weather(){
      axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.latitude}&lon=${this.longitude}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
       console.log(res.data)
        this.temp=Math.ceil((res.data.current.temp)-273);
        this.dew_point=res.data.current.dew_point;
        this.humidity=res.data.current.humidity;
        this.air_pressure=res.data.current.pressure;

        let sunriseTime=res.data.current.sunrise;
        let riseTime=new Date(sunriseTime*1000)
         this.sunrise=riseTime.toLocaleTimeString();


        let sunsetTime=res.data.current.sunset;
         let setTime=new Date(sunsetTime*1000)
         this.sunset=setTime.toLocaleTimeString();

        this.visibility=((res.data.current.visibility)/1000);
        
        let current_date=(res.data.current.dt);
        let time=new Date(current_date*1000)
         this.currentTime=time;

        this.windspeed=res.data.current.wind_speed;
        var icon=res.data.current.weather[0].icon;
        console.log(this.icon)
        var url=`http://openweathermap.org/img/w/${icon}.png`
        this.URL=url

//hourly

      
         let hourly_date1=(res.data.hourly[0].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[0].temp)-273);
        this.date3=Math.ceil((res.data.hourly[0].feels_like)-273)
        this.date4=res.data.hourly[0].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;

//2
   
         let hourly_date2=(res.data.hourly[1].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[1].temp)-273);
        this.date7=Math.ceil((res.data.hourly[1].feels_like)-273)
        this.date8=res.data.hourly[1].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[2].dt);
        let D3=new Date(hourly_date3*1000);
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[2].temp)-273);
        this.date11=Math.ceil((res.data.hourly[2].feels_like)-273)
        this.date12=res.data.hourly[2].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[3].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[3].temp)-273);
        this.date15=Math.ceil((res.data.hourly[3].feels_like)-273)
        this.date16=res.data.hourly[3].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[4].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
         
        this.date18=Math.ceil((res.data.hourly[4].temp)-273);
        this.date19=Math.ceil((res.data.hourly[4].feels_like)-273)
        this.date20=res.data.hourly[4].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[5].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[5].temp)-273);
        this.date23=Math.ceil((res.data.hourly[5].feels_like)-273)
        this.date24=res.data.hourly[5].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[6].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
         
        this.date26=Math.ceil((res.data.hourly[6].temp)-273);
        this.date27=Math.ceil((res.data.hourly[6].feels_like)-273)
        this.date28=res.data.hourly[6].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[7].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[7].temp)-273);
        this.date31=Math.ceil((res.data.hourly[7].feels_like)-273)
        this.date32=res.data.hourly[6].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 


        
//daily

      //1
         let Daily_date1=(res.data.daily[0].dt);
        let day1=new Date(Daily_date1*1000);
        this.daily1=day1.toLocaleDateString()
         
        this.daily2=Math.ceil((res.data.daily[0].temp.day)-273);
        this.daily3=Math.ceil((res.data.daily[0].feels_like.day)-273);
        this.daily4=res.data.daily[0].weather[0].icon;

        var urld1=`http://openweathermap.org/img/w/${this.daily4}.png`
        this.URLD1=urld1;


        //2
        let Daily_date2=(res.data.daily[1].dt);
        let day2=new Date(Daily_date2*1000);
        this.daily5=day2.toLocaleDateString();
     
        this.daily6=Math.ceil((res.data.daily[1].temp.day)-273);
        this.daily7=Math.ceil((res.data.daily[1].feels_like.day)-273);
        this.daily8=res.data.daily[1].weather[0].icon;

        var urld2=`http://openweathermap.org/img/w/${this.daily8}.png`
        this.URLD2=urld2;

//3

        let Daily_date3=(res.data.daily[2].dt);
        let day3=new Date(Daily_date3*1000);
        this.daily9=day3.toLocaleDateString();
     
        this.daily10=Math.ceil((res.data.daily[2].temp.day)-273);
        this.daily11=Math.ceil((res.data.daily[2].feels_like.day)-273);
        this.daily12=res.data.daily[2].weather[0].icon;

        var urld3=`http://openweathermap.org/img/w/${this.daily12}.png`
        this.URLD3=urld3;

        //4
           let Daily_date4=(res.data.daily[3].dt);
        let day4=new Date(Daily_date4*1000);
        this.daily13=day4.toLocaleDateString();
     
        this.daily14=Math.ceil((res.data.daily[3].temp.day)-273);
        this.daily15=Math.ceil((res.data.daily[3].feels_like.day)-273);
        this.daily16=res.data.daily[3].weather[0].icon;

        var urld4=`http://openweathermap.org/img/w/${this.daily16}.png`
        this.URLD4=urld4;


//5
let Daily_date5=(res.data.daily[4].dt);
        let day5=new Date(Daily_date5*1000);
        this.daily17=day5.toLocaleDateString();
     
        this.daily18=Math.ceil((res.data.daily[4].temp.day)-273);
        this.daily19=Math.ceil((res.data.daily[4].feels_like.day)-273);
        this.daily20=res.data.daily[4].weather[0].icon;

        var urld5=`http://openweathermap.org/img/w/${this.daily20}.png`
        this.URLD5=urld5;

        //6
        let Daily_date6=(res.data.daily[5].dt);
        let day6=new Date(Daily_date6*1000);
        this.daily21=day6.toLocaleDateString();
     
        this.daily22=Math.ceil((res.data.daily[5].temp.day)-273);
        this.daily23=Math.ceil((res.data.daily[5].feels_like.day)-273);
        this.daily24=res.data.daily[5].weather[0].icon;

        var urld6=`http://openweathermap.org/img/w/${this.daily24}.png`
        this.URLD6=urld6;

        //7
        let Daily_date7=(res.data.daily[6].dt);
        let day7=new Date(Daily_date7*1000);
        this.daily25=day7.toLocaleDateString();
     
        this.daily26=Math.ceil((res.data.daily[6].temp.day)-273);
        this.daily27=Math.ceil((res.data.daily[6].feels_like.day)-273);
        this.daily28=res.data.daily[6].weather[0].icon;

        var urld7=`http://openweathermap.org/img/w/${this.daily28}.png`
        this.URLD7=urld7;

         //8

        let Daily_date8=(res.data.daily[7].dt);
        let day8=new Date(Daily_date8*1000);
        this.daily29=day8.toLocaleDateString();
     
        this.daily30=Math.ceil((res.data.daily[7].temp.day)-273);
        this.daily31=Math.ceil((res.data.daily[7].feels_like.day)-273);
        this.daily32=res.data.daily[7].weather[0].icon;

        var urld8=`http://openweathermap.org/img/w/${this.daily32}.png`
        this.URLD8=urld8;


   

      })
    },
      cityName(){
      axios.get(`https://api.openweathermap.org/data/2.5/weather?lat=${this.latitude}&lon=${this.longitude}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
        //console.log(res.data)
       this.city_Name=res.data.name;
      //console.log(res.data.name)
     

      })
    },
    getValue(){
    
     axios.get(`https://api.openweathermap.org/data/2.5/weather?q=${this.inputvalue}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
      
       console.log(res.data)
       this.lat=res.data.coord.lat;
       this.long=res.data.coord.lon;
       
       localStorage.setItem("latitude",JSON.stringify(this.lat))
       localStorage.setItem("longitude",JSON.stringify(this.long))
        this.city_Name=res.data.name;

       this.getByname()
      
       this.inputvalue=''
     
      })

    },
    getByname(){
    
     axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.lat}&lon=${this.long}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
       console.log(res.data)
        this.temp=Math.ceil((res.data.current.temp)-273);
        this.dew_point=res.data.current.dew_point;
        this.humidity=res.data.current.humidity;
        this.air_pressure=res.data.current.pressure;

        let sunriseTime=res.data.current.sunrise;
        let riseTime=new Date(sunriseTime*1000)
         this.sunrise=riseTime.toLocaleTimeString();


        let sunsetTime=res.data.current.sunset;
         let setTime=new Date(sunsetTime*1000)
         this.sunset=setTime.toLocaleTimeString();

        this.visibility=((res.data.current.visibility)/1000);
        
        let current_date=(res.data.current.dt);
        let time=new Date(current_date*1000)
         this.currentTime=time;

        this.windspeed=res.data.current.wind_speed;
        var icon=res.data.current.weather[0].icon;
        console.log(this.icon)
        var url=`http://openweathermap.org/img/w/${icon}.png`
        this.URL=url;

        //hourly

      
         let hourly_date1=(res.data.hourly[0].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[0].temp)-273);
        this.date3=Math.ceil((res.data.hourly[0].feels_like)-273)
        this.date4=res.data.hourly[0].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;

//2
   
         let hourly_date2=(res.data.hourly[1].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[1].temp)-273);
        this.date7=Math.ceil((res.data.hourly[1].feels_like)-273)
        this.date8=res.data.hourly[1].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[2].dt);
        let D3=new Date(hourly_date3*1000);
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[2].temp)-273);
        this.date11=Math.ceil((res.data.hourly[2].feels_like)-273)
        this.date12=res.data.hourly[2].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[3].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[3].temp)-273);
        this.date15=Math.ceil((res.data.hourly[3].feels_like)-273)
        this.date16=res.data.hourly[3].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[4].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
         
        this.date18=Math.ceil((res.data.hourly[4].temp)-273);
        this.date19=Math.ceil((res.data.hourly[4].feels_like)-273)
        this.date20=res.data.hourly[4].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[5].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[5].temp)-273);
        this.date23=Math.ceil((res.data.hourly[5].feels_like)-273)
        this.date24=res.data.hourly[5].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[6].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
         
        this.date26=Math.ceil((res.data.hourly[6].temp)-273);
        this.date27=Math.ceil((res.data.hourly[6].feels_like)-273)
        this.date28=res.data.hourly[6].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[7].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[7].temp)-273);
        this.date31=Math.ceil((res.data.hourly[7].feels_like)-273)
        this.date32=res.data.hourly[6].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 


        
//daily

      //1
         let Daily_date1=(res.data.daily[0].dt);
        let day1=new Date(Daily_date1*1000);
        this.daily1=day1.toLocaleDateString()
         
        this.daily2=Math.ceil((res.data.daily[0].temp.day)-273);
        this.daily3=Math.ceil((res.data.daily[0].feels_like.day)-273);
        this.daily4=res.data.daily[0].weather[0].icon;

        var urld1=`http://openweathermap.org/img/w/${this.daily4}.png`
        this.URLD1=urld1;


        //2
        let Daily_date2=(res.data.daily[1].dt);
        let day2=new Date(Daily_date2*1000);
        this.daily5=day2.toLocaleDateString();
     
        this.daily6=Math.ceil((res.data.daily[1].temp.day)-273);
        this.daily7=Math.ceil((res.data.daily[1].feels_like.day)-273);
        this.daily8=res.data.daily[1].weather[0].icon;

        var urld2=`http://openweathermap.org/img/w/${this.daily8}.png`
        this.URLD2=urld2;

//3

        let Daily_date3=(res.data.daily[2].dt);
        let day3=new Date(Daily_date3*1000);
        this.daily9=day3.toLocaleDateString();
     
        this.daily10=Math.ceil((res.data.daily[2].temp.day)-273);
        this.daily11=Math.ceil((res.data.daily[2].feels_like.day)-273);
        this.daily12=res.data.daily[2].weather[0].icon;

        var urld3=`http://openweathermap.org/img/w/${this.daily12}.png`
        this.URLD3=urld3;

        //4
           let Daily_date4=(res.data.daily[3].dt);
        let day4=new Date(Daily_date4*1000);
        this.daily13=day4.toLocaleDateString();
     
        this.daily14=Math.ceil((res.data.daily[3].temp.day)-273);
        this.daily15=Math.ceil((res.data.daily[3].feels_like.day)-273);
        this.daily16=res.data.daily[3].weather[0].icon;

        var urld4=`http://openweathermap.org/img/w/${this.daily16}.png`
        this.URLD4=urld4;


//5
let Daily_date5=(res.data.daily[4].dt);
        let day5=new Date(Daily_date5*1000);
        this.daily17=day5.toLocaleDateString();
     
        this.daily18=Math.ceil((res.data.daily[4].temp.day)-273);
        this.daily19=Math.ceil((res.data.daily[4].feels_like.day)-273);
        this.daily20=res.data.daily[4].weather[0].icon;

        var urld5=`http://openweathermap.org/img/w/${this.daily20}.png`
        this.URLD5=urld5;

        //6
        let Daily_date6=(res.data.daily[5].dt);
        let day6=new Date(Daily_date6*1000);
        this.daily21=day6.toLocaleDateString();
     
        this.daily22=Math.ceil((res.data.daily[5].temp.day)-273);
        this.daily23=Math.ceil((res.data.daily[5].feels_like.day)-273);
        this.daily24=res.data.daily[5].weather[0].icon;

        var urld6=`http://openweathermap.org/img/w/${this.daily24}.png`
        this.URLD6=urld6;

        //7
        let Daily_date7=(res.data.daily[6].dt);
        let day7=new Date(Daily_date7*1000);
        this.daily25=day7.toLocaleDateString();
     
        this.daily26=Math.ceil((res.data.daily[6].temp.day)-273);
        this.daily27=Math.ceil((res.data.daily[6].feels_like.day)-273);
        this.daily28=res.data.daily[6].weather[0].icon;

        var urld7=`http://openweathermap.org/img/w/${this.daily28}.png`
        this.URLD7=urld7;

         //8

        let Daily_date8=(res.data.daily[7].dt);
        let day8=new Date(Daily_date8*1000);
        this.daily29=day8.toLocaleDateString();
     
        this.daily30=Math.ceil((res.data.daily[7].temp.day)-273);
        this.daily31=Math.ceil((res.data.daily[7].feels_like.day)-273);
        this.daily32=res.data.daily[7].weather[0].icon;

        var urld8=`http://openweathermap.org/img/w/${this.daily32}.png`
        this.URLD8=urld8;

      })

    },
    showHourly(){
    this.dataHourly=true;
    this.dataDaily=false;

    },
    showDaily(){
     this.dataHourly=false;
    this.dataDaily=true;

    },
    next(){
        this.nextclick++
        if(this.saveDatalat==null || this.saveDatalong==null){
             axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.latitude}&lon=${this.longitude}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
               let hourly_date1=(res.data.hourly[this.nextclick>1?this.i+16:this.i+8].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[this.nextclick>1?this.i+16:this.i+8].temp)-273);
        this.date3=Math.ceil((res.data.hourly[this.nextclick>1?this.i+16:this.i+8].feels_like)-273)
        this.date4=res.data.hourly[this.nextclick>1?this.i+16:this.i+8].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;
        //2
   
         let hourly_date2=(res.data.hourly[this.nextclick>1?this.j+16:this.j+8].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[this.nextclick>1?this.j+16:this.j+8].temp)-273);
        this.date7=Math.ceil((res.data.hourly[this.nextclick>1?this.j+16:this.j+8].feels_like)-273)
        this.date8=res.data.hourly[this.nextclick>1?this.j+16:this.j+8].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[this.nextclick>1?this.k+16:this.k+8].dt);
        let D3=new Date(hourly_date3*1000);
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[this.nextclick>1?this.k+16:this.k+8].temp)-273);
        this.date11=Math.ceil((res.data.hourly[this.nextclick>1?this.k+16:this.k+8].feels_like)-273)
        this.date12=res.data.hourly[this.nextclick>1?this.k+16:this.k+8].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[this.nextclick>1?this.l+16:this.l+8].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[this.nextclick>1?this.l+16:this.l+8].temp)-273);
        this.date15=Math.ceil((res.data.hourly[this.nextclick>1?this.l+16:this.l+8].feels_like)-273)
        this.date16=res.data.hourly[this.nextclick>1?this.l+16:this.l+8].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[this.nextclick>1?this.m+16:this.m+8].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
         
        this.date18=Math.ceil((res.data.hourly[this.nextclick>1?this.m+16:this.m+8].temp)-273);
        this.date19=Math.ceil((res.data.hourly[this.nextclick>1?this.m+16:this.m+8].feels_like)-273)
        this.date20=res.data.hourly[this.nextclick>1?this.m+16:this.m+8].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[this.nextclick>1?this.n+16:this.n+8].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[this.nextclick>1?this.n+16:this.n+8].temp)-273);
        this.date23=Math.ceil((res.data.hourly[this.nextclick>1?this.n+16:this.n+8].feels_like)-273)
        this.date24=res.data.hourly[this.nextclick>1?this.n+16:this.n+8].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[this.nextclick>1?this.o+16:this.o+8].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
         
        this.date26=Math.ceil((res.data.hourly[this.nextclick>1?this.o+16:this.o+8].temp)-273);
        this.date27=Math.ceil((res.data.hourly[this.nextclick>1?this.o+16:this.o+8].feels_like)-273)
        this.date28=res.data.hourly[this.nextclick>1?this.o+16:this.o+8].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[this.nextclick>1?this.p+16:this.p+8].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[this.nextclick>1?this.p+16:this.p+8].temp)-273);
        this.date31=Math.ceil((res.data.hourly[this.nextclick>1?this.p+16:this.p+8].feels_like)-273)
        this.date32=res.data.hourly[this.nextclick>1?this.p+16:this.p+8].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 

             })
        }
        else
        {
       axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.saveDatalat}&lon=${this.saveDatalong}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
        let hourly_date1=(res.data.hourly[this.nextclick>1?this.i+16:this.i+8].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[this.nextclick>1?this.i+16:this.i+8].temp)-273);
        this.date3=Math.ceil((res.data.hourly[this.nextclick>1?this.i+16:this.i+8].feels_like)-273)
        this.date4=res.data.hourly[this.nextclick>1?this.i+16:this.i+8].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;
        //2
   
         let hourly_date2=(res.data.hourly[this.nextclick>1?this.j+16:this.j+8].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[this.nextclick>1?this.j+16:this.j+8].temp)-273);
        this.date7=Math.ceil((res.data.hourly[this.nextclick>1?this.j+16:this.j+8].feels_like)-273)
        this.date8=res.data.hourly[this.nextclick>1?this.j+16:this.j+8].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[this.nextclick>1?this.k+16:this.k+8].dt);
        let D3=new Date(hourly_date3*1000);
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[this.nextclick>1?this.k+16:this.k+8].temp)-273);
        this.date11=Math.ceil((res.data.hourly[this.nextclick>1?this.k+16:this.k+8].feels_like)-273)
        this.date12=res.data.hourly[this.nextclick>1?this.k+16:this.k+8].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[this.nextclick>1?this.l+16:this.l+8].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[this.nextclick>1?this.l+16:this.l+8].temp)-273);
        this.date15=Math.ceil((res.data.hourly[this.nextclick>1?this.l+16:this.l+8].feels_like)-273)
        this.date16=res.data.hourly[this.nextclick>1?this.l+16:this.l+8].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[this.nextclick>1?this.m+16:this.m+8].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
         
        this.date18=Math.ceil((res.data.hourly[this.nextclick>1?this.m+16:this.m+8].temp)-273);
        this.date19=Math.ceil((res.data.hourly[this.nextclick>1?this.m+16:this.m+8].feels_like)-273)
        this.date20=res.data.hourly[this.nextclick>1?this.m+16:this.m+8].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[this.nextclick>1?this.n+16:this.n+8].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[this.nextclick>1?this.n+16:this.n+8].temp)-273);
        this.date23=Math.ceil((res.data.hourly[this.nextclick>1?this.n+16:this.n+8].feels_like)-273)
        this.date24=res.data.hourly[this.nextclick>1?this.n+16:this.n+8].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[this.nextclick>1?this.o+16:this.o+8].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
         
        this.date26=Math.ceil((res.data.hourly[this.nextclick>1?this.o+16:this.o+8].temp)-273);
        this.date27=Math.ceil((res.data.hourly[this.nextclick>1?this.o+16:this.o+8].feels_like)-273)
        this.date28=res.data.hourly[this.nextclick>1?this.o+16:this.o+8].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[this.nextclick>1?this.p+16:this.p+8].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[this.nextclick>1?this.p+16:this.p+8].temp)-273);
        this.date31=Math.ceil((res.data.hourly[this.nextclick>1?this.p+16:this.p+8].feels_like)-273)
        this.date32=res.data.hourly[this.nextclick>1?this.p+16:this.p+8].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 

        

       })
     
        }
    },
    prev(){
      this.nextclick=0
      if(this.saveDatalat==null || this.saveDatalong==null){
         axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.latitude}&lon=${this.longitude}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
             let hourly_date1=(res.data.hourly[this.i].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[this.i].temp)-273);
        this.date3=Math.ceil((res.data.hourly[this.i].feels_like)-273)
        this.date4=res.data.hourly[this.i].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;
        //2
   
         let hourly_date2=(res.data.hourly[this.j].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[this.j].temp)-273);
        this.date7=Math.ceil((res.data.hourly[this.j].feels_like)-273)
        this.date8=res.data.hourly[this.j].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[this.k].dt);
        let D3=new Date(hourly_date3*1000)
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[this.k].temp)-273);
        this.date11=Math.ceil((res.data.hourly[this.k].feels_like)-273)
        this.date12=res.data.hourly[this.k].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[this.l].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[this.l].temp)-273);
        this.date15=Math.ceil((res.data.hourly[this.l].feels_like)-273)
        this.date16=res.data.hourly[this.l].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[this.m].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
        
        this.date18=Math.ceil((res.data.hourly[this.m].temp)-273);
        this.date19=Math.ceil((res.data.hourly[this.m].feels_like)-273)
        this.date20=res.data.hourly[this.m].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[this.n].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[this.n].temp)-273);
        this.date23=Math.ceil((res.data.hourly[this.n].feels_like)-273)
        this.date24=res.data.hourly[this.n].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[this.o].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
        
        this.date26=Math.ceil((res.data.hourly[this.o].temp)-273);
        this.date27=Math.ceil((res.data.hourly[this.o].feels_like)-273)
        this.date28=res.data.hourly[this.o].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[this.p].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[this.p].temp)-273);
        this.date31=Math.ceil((res.data.hourly[this.p].feels_like)-273)
        this.date32=res.data.hourly[this.p].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 

         })
      }
    else{
      axios.get(`https://api.openweathermap.org/data/2.5/onecall?lat=${this.saveDatalat}&lon=${this.saveDatalong}&appid=dad624d112b01d43844c2284c461e811`).then((res)=>{
        let hourly_date1=(res.data.hourly[this.i].dt);
        let D1=new Date(hourly_date1*1000);
        var Time1=D1.toLocaleTimeString();
        var newTime1 = new Date(new Date("2000/01/01 " + Time1).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
        this.date1=newTime1
         
        this.date2=Math.ceil((res.data.hourly[this.i].temp)-273);
        this.date3=Math.ceil((res.data.hourly[this.i].feels_like)-273)
        this.date4=res.data.hourly[this.i].weather[0].icon;

        var url1=`http://openweathermap.org/img/w/${this.date4}.png`
        this.URL1=url1;
        //2
   
         let hourly_date2=(res.data.hourly[this.j].dt);
        let D2=new Date(hourly_date2*1000);
            var Time2=D2.toLocaleTimeString();
    var newTime2 = new Date(new Date("2000/01/01 " + Time2).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date5=newTime2

         
        this.date6=Math.ceil((res.data.hourly[this.j].temp)-273);
        this.date7=Math.ceil((res.data.hourly[this.j].feels_like)-273)
        this.date8=res.data.hourly[this.j].weather[0].icon;

        var url2=`http://openweathermap.org/img/w/${this.date8}.png`
        this.URL2=url2;

//3
         let hourly_date3=(res.data.hourly[this.k].dt);
        let D3=new Date(hourly_date3*1000)
              var Time3=D3.toLocaleTimeString();
    var newTime3 = new Date(new Date("2000/01/01 " + Time3).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date9=newTime3

         
        this.date10=Math.ceil((res.data.hourly[this.k].temp)-273);
        this.date11=Math.ceil((res.data.hourly[this.k].feels_like)-273)
        this.date12=res.data.hourly[this.k].weather[0].icon;

        var url3=`http://openweathermap.org/img/w/${this.date12}.png`
        this.URL3=url3;

       //4
         let hourly_date4=(res.data.hourly[this.l].dt);
        let D4=new Date(hourly_date4*1000);
        var Time4=D4.toLocaleTimeString();
    var newTime4 = new Date(new Date("2000/01/01 " + Time4).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date13=newTime4
         
        this.date14=Math.ceil((res.data.hourly[this.l].temp)-273);
        this.date15=Math.ceil((res.data.hourly[this.l].feels_like)-273)
        this.date16=res.data.hourly[this.l].weather[0].icon;

        var url4=`http://openweathermap.org/img/w/${this.date16}.png`
        this.URL4=url4; 

             //5
         let hourly_date5=(res.data.hourly[this.m].dt);
        let D5=new Date(hourly_date5*1000);
        var Time5=D5.toLocaleTimeString();
    var newTime5 = new Date(new Date("2000/01/01 " + Time5).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date17=newTime5
        
        this.date18=Math.ceil((res.data.hourly[this.m].temp)-273);
        this.date19=Math.ceil((res.data.hourly[this.m].feels_like)-273)
        this.date20=res.data.hourly[this.m].weather[0].icon;

        var url5=`http://openweathermap.org/img/w/${this.date20}.png`
        this.URL5=url5; 

        
             //6
         let hourly_date6=(res.data.hourly[this.n].dt);
        let D6=new Date(hourly_date6*1000);
          var Time6=D6.toLocaleTimeString();
    var newTime6 = new Date(new Date("2000/01/01 " + Time6).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date21=newTime6
         
        this.date22=Math.ceil((res.data.hourly[this.n].temp)-273);
        this.date23=Math.ceil((res.data.hourly[this.n].feels_like)-273)
        this.date24=res.data.hourly[this.n].weather[0].icon;

        var url6=`http://openweathermap.org/img/w/${this.date24}.png`
        this.URL6=url6; 

               //7
         let hourly_date7=(res.data.hourly[this.o].dt);
        let D7=new Date(hourly_date7*1000);
          var Time7=D7.toLocaleTimeString();
    var newTime7 = new Date(new Date("2000/01/01 " + Time7).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date25=newTime7
        
        this.date26=Math.ceil((res.data.hourly[this.o].temp)-273);
        this.date27=Math.ceil((res.data.hourly[this.o].feels_like)-273)
        this.date28=res.data.hourly[this.o].weather[0].icon;

        var url7=`http://openweathermap.org/img/w/${this.date28}.png`
        this.URL7=url7; 

               //8
         let hourly_date8=(res.data.hourly[this.p].dt);
        let D8=new Date(hourly_date8*1000);
            var Time8=D8.toLocaleTimeString();
    var newTime8 = new Date(new Date("2000/01/01 " + Time8).getTime() + 45 * 60000).toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit', hour12: true });
    this.date29=newTime8
         
        this.date30=Math.ceil((res.data.hourly[this.p].temp)-273);
        this.date31=Math.ceil((res.data.hourly[this.p].feels_like)-273)
        this.date32=res.data.hourly[this.p].weather[0].icon;

        var url8=`http://openweathermap.org/img/w/${this.date32}.png`
        this.URL8=url8; 

       })
    }
      
    }
   
    
  },

  created(){
    this.findMyLocation()
  },

}

</script>


<style>

*{
  margin: 0;
}
body{
  font-family: 'Lato', sans-serif;
}
.currenttime{
  margin-top:-35px;
  margin-left:42px;
  width:300px;
  height:10vh
}
.sunset{
   margin-top:-25px;
   margin-left:42px;
}
.calendar{
  margin-top:10px;
  color:green
}
#img{
 background: url("https://images.pexels.com/photos/2589456/pexels-photo-2589456.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1") no-repeat center center fixed;
 filter: contrast(100%);
 filter:saturate(170%);
 height: 900px;
-webkit-background-size: cover;
-moz-background-size: cover;
-o-background-size: cover;
 background-size: cover;
 color: aqua;
  /* //background-image: url("https://images.pexels.com/photos/3454270/pexels-photo-3454270.jpeg?auto=compress&cs=tinysrgb&w=1500&h=900&dpr=1"); */
}
#inputSearch:focus{
    outline: none;
}
#div1{
padding-top: 2.5%;
 
  width: 15%;
  height: fit-content;
  margin-left: 2%;
  color: whitesmoke;
  display: inline-block;
   
}
#div1>img{
  transition: all .2s ease-in-out;

}
#div1>img:hover{
transform: scale(1.5);

}
#div1>h3{
  transition: all .2s ease-in-out;
}
#div1>h3:hover{
transform: scale(1.1);
}
#div1>span>p{
  transition: all .2s ease-in-out;
  
}
#div1>span>p:hover{
transform: scale(1.1);
}
#div1>h1{
font-family:Arial;
font-weight: bolder;
 font-size: 70px;
  transition: all .2s ease-in-out;
}
#div1>h1:hover{
transform: scale(1.1);
}
#div1>span>img{
 height: 35px;
 width: 35px;
}
#div1>span>#location{
 height: 30px;
  width: 30px;
  
}
#div2{
  display: inline-block;
  margin-left: 60%;
  vertical-align: top;
  
  margin-top: 5%;
  width: 15%;
  height: 25%;
   color: whitesmoke;
}
#humidty>img{
  height: 30px;
  width: 30px;
  margin-top:10px
}
#div2_1{
    transition: all .2s ease-in-out;
    margin-bottom: 10%;
  
}
#div2_1:hover{
transform: scale(1.1);
  
}
#humidty1{
  vertical-align: top;
font-weight: bolder;
  font-family:Arial ;
  font-size: 18px;
}

#div2_1>p{

  margin-left: 38px;
  font-weight: bolder;
  font-family:Arial ;
  font-size: 20px;
  margin-top:-20px
}
#div3{
  margin-top: 2%;
  text-align: center;
  
}
#div3_1{
box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
  display: inline-block;
  border:none;
  border-radius: 5px;
  height: 140px;
  width: 150px;
  margin-right: 15px;
  text-align: left;
  transition: all .2s ease-in-out;
}
#div3_1:hover{
transform: scale(1.1);
 
}
#div3_1>p:nth-child(1){
 font-weight: bolder;
  padding: 5px 0px 0px 10px;
}
#div3_1>h1{
 font-weight: bolder;
  padding: 10px 0px 0px 40px;
  font-family: Arial;
  font-weight: bolder;
 font-size: 25px;
}
#div3_1>p:nth-child(3){
  font-size: 13px;
  padding: 5px 0px 0px 25px;
}
#div3_1>p:nth-child(4){
  text-align: center;
}
#buttonChange{
  margin-top: 3%;
  margin-left: 6%;
}
#buttonChange>button{
  margin-right: 1%;
  border-radius: 10px;
 padding: 10px;
 box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
   background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    color:white;
    transition: all .2s ease-in-out;
}
#buttonChange>button:hover{
transform: scale(1.1);

}
#inputSearch{
background: url("../../icons/placeholder.png") no-repeat scroll 7px 7px;
padding-left:30px;
display: inline-block;
color:white;
height: 25px;
border-radius: 25px;

}
#inputButton1{
  display: inline-block;
  margin-top: 10px;
  margin-bottom: 10px;
   border-radius: 10px;
 padding: 10px;
 box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
   background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    color:white;
    transition: all .2s ease-in-out;
}
::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
  color: white;
  opacity: 1; /* Firefox */
}
#inside{
margin-left: 14.5%;
margin-top:-1.5% ;
position: absolute;
}
#hovering{
  transition: all .2s ease-in-out;
  
}
#hovering:hover{
transform: scale(1.5);
font-weight: bolder;

}
#hovering>img{
  transition: all .2s ease-in-out;
}
#hovering:hover>img{
transform: scale(1.2);

}


@media (min-width:350px) and (max-width:500px  ){
body{
  background-color:red;
}
#div1>h3{
  font-size: 15px;
}
#div1>h1{
font-family:Arial;
font-weight: bolder;
 font-size: 35px;
  
}
#div1>span>img{
 height: 25px;
 width: 25px;
}
#humidty>img{
  height: 25px;
  width: 25px;
}
#humidty1{
  vertical-align: top;
font-weight: bolder;
  font-family:Arial ;
  font-size: 16px;
}
#div2_1>p{

  margin-left: 10%;
font-weight: bolder;
  font-family:Arial ;
  font-size: 16px;
}
#div3_1{
box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
  display: inline-block;
  border:none;
  border-radius: 3px;
  height: 110px;
  width: 120px;
  margin-right: 10px;
  text-align: left;
  transition: all .2s ease-in-out;
}
#inputSearch{
 
padding-left:15px;
  display: inline-block;
color:white;
  height: 20px;
 border-radius: 25px;
 width: 140px;
}
#inside{
margin-left: 130px;
position: absolute;
margin-top: -20px;
}
#div2{
  display: inline-block;
  margin-left: 60%;
  vertical-align: top;
  
  margin-top: 5%;
  width: 20%;
  height: 25%;
   color: whitesmoke;
}
#hovering{
font-size: 14px;
}
#img{
  background: url("https://images.pexels.com/photos/2589456/pexels-photo-2589456.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1") no-repeat center center fixed;

height: 830px;
-webkit-background-size: cover;
-moz-background-size: cover;
-o-background-size: cover;
background-size: cover;
  color: aqua;
  /* //background-image: url("https://images.pexels.com/photos/3454270/pexels-photo-3454270.jpeg?auto=compress&cs=tinysrgb&w=1500&h=900&dpr=1"); */
}
#div3_1>p:nth-child(1){
 font-weight: bolder;
  padding: 5px 0px 0px 10px;
  font-size: 13px;
}
#div3_1>h1{
 font-weight: bolder;
  padding: 10px 0px 0px 40px;
  font-family: Arial;
  font-weight: bolder;
 font-size: 20px;
}
#div3_1>p:nth-child(3){
  font-size: 13px;
  padding: 5px 0px 0px 25px;
}
#div3_1>p:nth-child(4){
  text-align: center;
}
#buttonChange{
  margin-top: 3%;
  margin-left: 2%;
}
#buttonChange>button{
  margin-right: 1%;
  border-radius: 10px;
 padding: 10px;
 box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
   background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    color:white;
    transition: all .2s ease-in-out;
}
#buttonChange>button:hover{
transform: scale(1.1);

}
}


@media  (max-width:500px  ){
body{
  background-color:green;
}
#div1>h3{
  font-size: 15px;
}
#div1>h1{
font-family:Arial;
font-weight: bolder;
 font-size: 35px;
  
}
#div1>span>img{
 height: 25px;
 width: 25px;
}
#humidty>img{
  height: 25px;
  width: 25px;
}
#humidty1{
  vertical-align: top;
font-weight: bolder;
  font-family:Arial ;
  font-size: 16px;
}
#div2_1>p{

  margin-left: 10%;
font-weight: bolder;
  font-family:Arial ;
  font-size: 16px;
}
#div3_1{
box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
  display: inline-block;
  border:none;
  border-radius: 3px;
  height: 110px;
  width: 120px;
  margin-right: 10px;
  text-align: left;
  transition: all .2s ease-in-out;
}
#inputSearch{
 
padding-left:15px;
  display: inline-block;
color:white;
  height: 20px;
 border-radius: 25px;
 width: 140px;
}
#inside{
margin-left: 130px;
position: absolute;
margin-top: -20px;
}
#div2{
  display: inline-block;
  margin-left: 60%;
  vertical-align: top;
  
  margin-top: 5%;
  width: 20%;
  height: 25%;
   color: whitesmoke;
}
#hovering{
font-size: 14px;
}
#img{
  background: url("https://images.pexels.com/photos/2589456/pexels-photo-2589456.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1") no-repeat center center fixed;

height: 1200px;
-webkit-background-size: cover;
-moz-background-size: cover;
-o-background-size: cover;
background-size: cover;
  color: aqua;
  /* //background-image: url("https://images.pexels.com/photos/3454270/pexels-photo-3454270.jpeg?auto=compress&cs=tinysrgb&w=1500&h=900&dpr=1"); */
}
#div3_1>p:nth-child(1){
 font-weight: bolder;
  padding: 5px 0px 0px 10px;
  font-size: 13px;
}
#div3_1>h1{
 font-weight: bolder;
  padding: 10px 0px 0px 40px;
  font-family: Arial;
  font-weight: bolder;
 font-size: 20px;
}
#div3_1>p:nth-child(3){
  font-size: 13px;
  padding: 5px 0px 0px 25px;
}
#div3_1>p:nth-child(4){
  text-align: center;
}
#buttonChange{
  margin-top: 3%;
  margin-left: 2%;
}
#buttonChange>button{
  margin-right: 1%;
  border-radius: 10px;
 padding: 10px;
 box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
   background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    color:white;
    transition: all .2s ease-in-out;
}
#buttonChange>button:hover{
transform: scale(1.1);

}
}

@media (min-width:501px) and (max-width:1200px){
#img{
  height: 1000px;
}
#inside{
  position:absolute;
  margin-left:180px;
  margin-top: -20px;
}

}

</style>

