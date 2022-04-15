<template>
  <div id="app">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />
      <div id="first">  
        <h1 class="title">
          Hi ✌, <br>  
          I'm a <span style="text-shadow: 0px 0px 5px rgb(136, 0, 255);">full-stack</span>  dev.
        </h1>
      
        <i class="fa-solid fa-code" @click="toGithub"></i>
      

      </div>

      <div id="second">
          <h1 class="title">I use these framework {{'&'}} languages;</h1>
          <div class="techs">
            <i class="fa-brands fa-vuejs" style="color:#41B883"></i>

            <i class="fa-brands fa-react" style="color:skyblue"></i>

            <i class="fa-brands fa-js" style="color:orange"></i>

            <img src="https://www.svgrepo.com/show/303600/typescript-logo.svg" width="50px">
          </div>

          <img src="./assets/tothemoon.svg" alt="to the fuckin' moon" width="50%">
      </div>

      <div id="last">
          <h1 class="title">Reach me</h1>

          <input type="text" placeholder="Name">

          <input type="text" placeholder="Title">

          <textarea name="" cols="30" rows="10"></textarea>

          <button>send it</button>
      </div>

        <button class="up" @click="decrease" v-if="location !== '/' || location === '#first'">
            <i class="fa-solid fa-chevron-up"></i>      
        </button>

        <button class="down" @click="increase" v-if="location !== '#last'" >
            <i class="fa-solid fa-chevron-down"></i>      
        </button>
  </div>
</template>

<script>
export default {
  name: 'App',
  created(){
    document.title = 'Landing Page!'
    this.location = location.pathname
    console.log(this.location)
  },
  data(){
    return{
      location:''
    }
  },
  methods:{
    increase(){
      if(this.location === '#first' || this.location === '/'){
         this.location = '#second'
         return window.location.href = this.location
      }
      this.location = '#last'
      return window.location.href = this.location
    },
    decrease(){
      if(this.location === '#last'){
         this.location = '#second'
      return window.location.href = this.location
      }
      this.location = '/'
      return window.location.href = '#first'
    },
    toGithub(){
      window.location.href = 'https://github.com/yefee8';
    }
  }
  // components: {
  // }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@700&display=swap');

.title{
  font-family: Ubuntu, 'sans-serif';
  margin-top: 15%;
}

.fa-code{
  padding:30px;
  font-size: 200px;
  transition: 500ms;
  transform: rotate(0deg);
  margin-top: calc(15% - 30px);
  cursor: pointer;
}

.fa-code:hover{
  margin-top: calc(17.5% - 30px);
  margin-left:100px;
}

.up, .down{
  width: 50px;
  height: 50px;
  border: 2px solid #ffffff;
  background: transparent;
  border-radius: 100px;
  color: #ffffff;
  font-size: 25px;
  cursor: pointer;
  transition: 250ms;
}

.down{
  position: fixed;bottom: 50px;
}

.up{
  position: fixed;top:50px;
}

.down:hover, .up:hover{
  border: 2px solid rgb(136, 0, 255);
  color:rgb(136, 0, 255);
  filter: drop-shadow(0px 0px 15px rgb(136, 0, 255));
}

html{
  scroll-behavior: smooth;
  overflow: hidden;
}
body{
  color:#ffffff;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' version='1.1' xmlns:xlink='http://www.w3.org/1999/xlink' xmlns:svgjs='http://svgjs.com/svgjs' width='1440' height='560' preserveAspectRatio='none' viewBox='0 0 1440 560'%3e%3cg mask='url(%26quot%3b%23SvgjsMask2078%26quot%3b)' fill='none'%3e%3crect width='1440' height='560' x='0' y='0' fill='%230e2a47'%3e%3c/rect%3e%3cuse xlink:href='%23SvgjsSymbol2085' x='0' y='0'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsSymbol2085' x='720' y='0'%3e%3c/use%3e%3c/g%3e%3cdefs%3e%3cmask id='SvgjsMask2078'%3e%3crect width='1440' height='560' fill='white'%3e%3c/rect%3e%3c/mask%3e%3cpath d='M-1 0 a1 1 0 1 0 2 0 a1 1 0 1 0 -2 0z' id='SvgjsPath2082'%3e%3c/path%3e%3cpath d='M-3 0 a3 3 0 1 0 6 0 a3 3 0 1 0 -6 0z' id='SvgjsPath2084'%3e%3c/path%3e%3cpath d='M-5 0 a5 5 0 1 0 10 0 a5 5 0 1 0 -10 0z' id='SvgjsPath2079'%3e%3c/path%3e%3cpath d='M2 -2 L-2 2z' id='SvgjsPath2083'%3e%3c/path%3e%3cpath d='M6 -6 L-6 6z' id='SvgjsPath2081'%3e%3c/path%3e%3cpath d='M30 -30 L-30 30z' id='SvgjsPath2080'%3e%3c/path%3e%3c/defs%3e%3csymbol id='SvgjsSymbol2085'%3e%3cuse xlink:href='%23SvgjsPath2079' x='30' y='30' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='30' y='90' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2080' x='30' y='150' stroke='%231c538e' stroke-width='3'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='30' y='210' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='30' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='30' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='30' y='390' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='30' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='30' y='510' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='30' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='90' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='90' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='90' y='150' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='90' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='90' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='90' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='90' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='90' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='90' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='90' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='150' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='150' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='150' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='150' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='150' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='150' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='150' y='390' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='150' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='150' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='150' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='210' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='210' y='90' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='210' y='150' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='210' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='210' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='210' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='210' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='210' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='210' y='510' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='210' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='270' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='270' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='270' y='150' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='270' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='270' y='270' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='270' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='270' y='390' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='270' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='270' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='270' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='330' y='30' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='330' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='330' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='330' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='330' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='390' y='30' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='390' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='390' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='390' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='390' y='270' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='390' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='390' y='390' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='390' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='390' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='390' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='450' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='450' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='450' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2080' x='450' y='210' stroke='rgba(220%2c 20%2c 60%2c 1)' stroke-width='3'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='450' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='450' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='450' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='450' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='450' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='450' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='510' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='510' y='90' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='510' y='150' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='510' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='510' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='510' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='510' y='390' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='510' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2080' x='510' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)' stroke-width='3'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='510' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='570' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='570' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='210' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='570' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='570' y='510' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='570' y='570' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='630' y='30' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='630' y='90' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='630' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='630' y='210' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='630' y='270' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='630' y='330' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='630' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='630' y='450' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='630' y='510' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='630' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2080' x='690' y='30' stroke='rgba(220%2c 20%2c 60%2c 1)' stroke-width='3'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='690' y='90' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='690' y='150' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='690' y='210' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2083' x='690' y='270' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2082' x='690' y='330' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='690' y='390' stroke='%231c538e'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2081' x='690' y='450' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2079' x='690' y='510' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3cuse xlink:href='%23SvgjsPath2084' x='690' y='570' stroke='rgba(220%2c 20%2c 60%2c 1)'%3e%3c/use%3e%3c/symbol%3e%3c/svg%3e");
}
#app{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

#first, #second, #last{
display: flex;
flex-direction: column;
align-items: center;
width: 100vh;
height: 100vh;
}


#second{
  margin-top: 100%;
}

#last{
  margin-top:200%;
}

.techs{
  margin-top: 10%;
  font-size: 50px;
  display: flex;
  width: 100vh;
  justify-content: space-evenly;
}

.techs > i, .techs > img{
  cursor: pointer;
  transition: 250ms;
}

.techs > i:hover{
  font-size: 60px;
}

.techs > img:hover{
  width: 60px;
}

#second > img{
  transition: 500ms;
  margin-top:5%; 
  cursor: pointer;
  border-radius:500px;
}
#second > img:hover{
  margin-top:7.5%; 
  margin-left:100px;
}

textarea, input{
    transition: 250ms;
    margin-top: 5%;
    width:400px;
    height: 40px;
    font-size:20px;
    border: 0px;
    text-align: center;
    border-radius: 10px;
}

textarea{
  height: 100px;
  text-align: left;
}

textarea:focus, input:focus{
  border: 0px;
  outline: none;
  margin-left: 50px;
  box-shadow: 0px 0px 10px 0px rgb(136, 0, 255);
}

#last > button{
  width: 200px;
  height: 50px;
  border: 3px solid rgb(136, 0, 255);
  background: transparent;
  border-radius: 10px;
  font-size: 20px;
  margin-top: 5%;
  cursor: pointer;
  transition: 250ms;
  color: white;
  background: rgb(136, 0, 255);
}
#last > button:hover, #last > button:focus{
  margin-left: 50px;
}
</style>
