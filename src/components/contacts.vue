<template>
<span v-touch:swipe.right="swipeHandlerRight">


    <slider></slider>
    <anag></anag>
    <div style="height:800px">
      <div class="text">
        <h2>Informazioni</h2>
        <p>Per qualsiasi informazione puoi contattarmi alla seguente mail: <span id="mail">{{ mail }}</span> </p>
        <br>
        <p>Di seguito sono presenti i link ai miei vari social e il mio profilo github in cui pubblico i miei ultimi lavori.</p>
          <div>
                <span>Facebook: </span>
                <a href="https://www.facebook.com/xXEnricoXx" target="_blank">
                  <img src="src/assets/facebook.png" width="24" height="24" />
                </a><br><br>
                <span>Instagram: </span>
                <a href="https://www.instagram.com/enri_sedo/?hl=it" target="_blank">
                  <img src="src/assets/instagram.png" width="24" height="24" />
                </a><br><br>
                <span>Linkedin: </span>
                <a href="https://www.linkedin.com/in/enrico-sedoni-0818ab12b/" target="_blank">
                  <img src="src/assets/linkedin.png" width="24" height="24" />
                </a><br><br>
                <span>Github: </span>
                <a href="https://github.com/enrico404" target="_blank">
                  <img src="src/assets/github.png" width="24" height="24" />
                </a>
              </div>
              <div class="aboutImm">
              <img src="src/assets/info.png" width="120" height="120"  />
            </div>
      </div>
    </div>
</span>
</template>

<script>

import Slider from './slider'
import Anag from './anag'


export default {

  components:{
    'anag':Anag,
    'slider':Slider


  },

  data () {
    return {

        mail:'sedoni.enrico@gmail.com'

    }
  },
  methods:{

    swipeHandlerRight(){

      
      this.$router.push('/blog');

    },

  }
}
</script>


<style scoped>
.aboutImm{
  float: right;
  margin-right: 100px;
  margin-top: -80px;

}
.text{
  padding: 20px 20px;
  width: 100%;
  margin-left: 0px;
  border-radius: 0px;
  margin-top: 320px;
  height: 565px;
  background-color: #3498db;
  opacity: 0;
  animation-name: entry;
  animation-duration:0.4s;
  animation-timing-function: ease-in;
  animation-fill-mode: forwards;


}
@keyframes entry{

  from{
    opacity: 0;
  }to{
    opacity: 1;
  }

}

a{
  margin-left: 10px;

}

h2{
text-align: center;
padding-bottom: 20px;
font-weight: bold;
}

#mail{
  font-weight: bold;

}
p, span {
  font-size: 11pt;
}

@media (max-width:992px ){

  .text{
    width: 100vw;
    margin-left: 0px;
    border-radius: 0px;
    /* margin-top: 300px; */
    height: 500px;

  }


}

@media(max-width: 576px){
  .aboutImm{
    display: none;
  }


}



</style>
