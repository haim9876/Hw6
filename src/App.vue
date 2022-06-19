<template>
 <div>
    <h1 id = "title">
      Click On The Swap Button To Switch The Images
    </h1>
    <div><button id="button1" @click="swapFunc">Swap</button></div>
    <div id="app">
      <img :src="pictureHover1" @mouseover="hover1=true" @mouseleave="hover1=false" width="350" height="500" />
      <br />
      <br />
      <img :src="pictureHover2" @mouseover="hover2=true" @mouseleave="hover2=false" width="450" height="400" />
      <br />
      <br />
      <img :src="pictureHover3" @mouseover="hover3=true" @mouseleave="hover3=false" width="300" height="500" />
      <br />
      <br />
      <img :src="pictureHover4" @mouseover="hover4=true" @mouseleave="hover4=false" width="350" height="500" />
    </div>
  </div>
</template>

<script>

export default {
  name: "App",
  
  data() {
      return {
        image1: "/1.jpg",
				image2: "/2.jpg",
        image3: "/3.jpg",
        image4: "/4.jpg",
        image5: "/5.jpg",
				image6: "/6.jpg",
        image7: "/7.jpg",
        image8: "/8.jpg",
				hover1: false,
        hover2: false,
        hover3: false,
        hover4: false,
        flag: false
      }
    },
    computed: {
      pictureHover1() {
        if(this.hover1 == true) {
          return this.image5
        }
        else {
          return this.image1
        }
      },
      pictureHover2() {
        if(this.hover2 == true) {
          return this.image6
        }
        else {
          return this.image2
        }
      },
      pictureHover3() {
        if(this.hover3 == true) {
          return this.image7
        }
        else {
          return this.image3
        }
      },
      pictureHover4() {
        if(this.hover4 == true) {
          return this.image8
        }
        else {
          return this.image4
        }
      }
    },
    methods: {
      swapFunc() {
        this.flag = !this.flag
        if(this.flag == true) {
          this.image1 = "/5.jpg",
          this.image2 = "/6.jpg",
          this.image3 = "/7.jpg",
          this.image4 = "/8.jpg",
          this.image5 = "/1.jpg",
          this.image6 = "/2.jpg",
          this.image7 = "/3.jpg",
          this.image8 = "/4.jpg"
        }
        else {
          this.image1 = "/1.jpg",
          this.image2 = "/2.jpg",
          this.image3 = "/3.jpg",
          this.image4 = "/4.jpg",
          this.image5 = "/5.jpg",
          this.image6 = "/6.jpg",
          this.image7 = "/7.jpg",
          this.image8 = "/8.jpg"
        }
      }
    }
};
</script>
<style scoped>
  #button1 {
    background-color: blue;
    border: none;
    color: white;
    padding: 30px 60px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 32px;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    margin-left: 45%;
    margin-top: 40px;
  }
  #button1:hover {
    background-color: #5cAFff;
  }
  img {
    border-radius: 15px;
    border: 1px solid #ffffff;
    float: left;
    margin-left: 50px;
    margin-top: 80px;
  }
  #title{
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    text-align: center;
    color: brown;
    margin-top: 60px;
  }
</style>