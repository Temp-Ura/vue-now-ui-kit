<template>
  <div class="starter-page">
    <div class="section text-center">
      <img id="header" src="/img2/prendiamola-con-filosofia-header.jpg" alt="">
      <!--<h1>
          Prendiamo con Filosofia
      </h1>
      <h3> 
          Strumenti pratici per affrontare la quarantena
      </h3>
      <h2> 
          28 Marzo
      </h2>-->
      <div id="manif">
        <iframe class="video" src="https://www.youtube.com/embed/05A9axDrWeY?controls=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="programma" >
        <h2 id="tito"> PROGRAMMA </h2>
        <h4 id="data"> 21 marzo </h4>
        <section class="tab_prog" v-for="item in prog" :key="item">
            <img class="profile_img" :src="'/img-rel/' + item.immagine" />
            <div class="text_prog">
            <h3 class="orario"> {{item.orario_inizio}} - {{item.orario_fine}} </h3>
            <h4 class="titolo"> {{item.titolo}} </h4>
            <h4 class="inter"> {{item.interviene}} </h4>
            <h5 class="mod" v-if="item.modera != '' "> Modera {{item.modera}} </h5>
            </div>
        </section>
      </div>
      <div class="sponsor" id="partner">
        <h2 id="tito">UN PROGETTO DI</h2>
        <section class="loghi-1">
          <img class="logo-1" src="/img2/logo-pianob.png">
          <img class="logo-1" src="/img2/Logo_Tlon_BLack.png">
        </section>
      </div>
    </div>
  </div>
</template>
<script>
//import json from "./prog.json";
export default {
  name: 'starter',
  data(){
    return{
    prog:[
  {
    "orario_inizio": "13:00",
    "orario_fine": "13:30",
    "titolo": "Roba Bella",
    "interviene": "Tizio Caio",
    "modera": "Giovanni",
    "intro": "Parliamo di roba bella perchè è importante",
    "immagine": "foto-lucrezia-ercoli.jpg"
  },
  {
    "orario_inizio": "13:30",
    "orario_fine": "14:00",
    "titolo": "Cose Importanti",
    "interviene": "Paolo Bianchi",
    "modera": "",
    "intro": "",
    "immagine": "foto-lucrezia-ercoli.jpg"
  }
]
    };
  },

  // created(){
  //   this.prog= "./prog.json";
  //   console.log(this.prog);
  // }
};
</script>
<style>
.starter-page {
  min-height: calc(100vh - 95px);
}

.video{
        /*position: absolute;*/
        top: 0;
        left: 0;
        width: 100%;
        height: 56vw;
        border: 20px solid #259B92;
        
    }

    body{
      margin: 0;
    }

    #tito{
      color:  #259B92;
      margin-top: 30px;
      margin-bottom: 0px;
      font-weight: 900;
      font-size: 40px;
    }

    #data{
      margin-top: 0px;
      font-weight: 200;
      font-size: 30px;
      /* color:  #259B92;
      
      font-weight: 900;
      font-size: 50px; */
    }

    .profile_img{
      
      float: left;
      width: 200px;
      height: 200px;
      margin-right: 20px;
      border: 5px solid #259B92;
    }

    .tab_prog{
      display: flex;
      /* border: 5px solid #259B92; */
      direction: row;
      justify-content:start;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }
    .text_prog{
      text-align: left;
      float: right;  
      min-width: 200px;    
    }
    
    .programma{
      margin: 0 25vw 0 25vw;
      text-align: left;
    }

    .orario{
      color:  #259B92;
      margin-bottom: 0px;
    }

    .titolo{
      font-size: 30px;
      margin-top: 0px;
    }

    .inter{
      margin-top: 0;
      margin-bottom: 0;
      font-size: 30px;
      font-weight: 800;
    }

    .mod{
      margin-top: 0;
      font-size: 20px;
      font-weight: 300;
    }

    .sponsor{
      margin: 0 25vw 0 25vw;
      text-align: left;
    }

    .logo-1{
      width: 200px;
      margin: 30px 50px 0 0;
    }
</style>
