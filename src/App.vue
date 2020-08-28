<template>
 <div id="app">
    <HelloWorld msg="U LIKE THIS ?" />
    <br>
    <div class="row">
      <div class="col-12">
      <img src="https://freedom.ilaw.or.th/sites/default/files/imagecache/wysiwyg_imageupload_colorbox_preset/wysiwyg_imageupload/1/02_3.jpg" width="200" height="200" />
        <h1>{{total1}}</h1>
        <div class="col-12">
          <CsButton @cc="sum" /><br>
        </div>
      </div>
      <div class="col-12">
      <img src="https://media0.giphy.com/media/3osxYuTGietZW1qBfa/200w.webp?cid=ecf05e47cykyeupgh4706qlu3wqqi2tb9vocpp33lgdd8h03&rid=200w.webp" width="200" height="200" />
        <h1>{{total2}}</h1>
        <div class="col-12">
          <CsButton @cc="sum1" />
        </div>
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CsButton";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sum1(counterValue){
    this.total2 = counterValue
},
},

};

</script>

<style>
body {
      background-image: url(https://media1.tenor.com/images/8e46150f790fbefe438d9c2767c32ad1/tenor.gif?itemid=15673753);
      background-size: 100px 100px ;
    }
#app {
  font-family: 'Londrina Solid', cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 70px;
}
</style>