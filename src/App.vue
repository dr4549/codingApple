<template>

  <Modal :원룸들="원룸들" :누른거="누른거" :모달창열렸니="모달창열렸니"/>



  <div class="menu">
    <a v-for="메뉴들 in menus" :key="메뉴들">{{ 메뉴들 }}</a>  
    </div>

  <Discount/>



 <Card :원룸="원룸들[i]" v-for="(작명,i) in 원룸들" :key="작명"/>

 <!-- <Card :원룸="원룸들[1]"/>
 <Card :원룸="원룸들[2]"/>
 <Card :원룸="원룸들[3]"/>
 <Card :원룸="원룸들[4]"/>
 <Card :원룸="원룸들[5]"/> -->

  <!-- <div v-for="(데이터,i) in 원룸들" :key="i">
    <img :src="데이터.image" class="room-img">
    <h4 @click="모달창열렸니 = true; 누른거 = i ">{{데이터.title}}</h4>
  -->

  <!--
 <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{products[0]}}</h4>
    <p> 60 만원</p>
    <button @click="신고수[1]++">허위매물신고</button> 
    <span>신고수 : {{신고수[1]}}</span>
  </div>
  
  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{products[0]}}</h4>
    <p> 70 만원</p>
    <button @click="신고수[2]++">허위매물신고</button> 
    <span>신고수 : {{신고수[2]}}</span>
  </div>
  -->
</template>

<script>

import data from './assets/oneroom.js';
import Discount from './Discount.vue'; // vue 파일 import 등록
import Modal from './Modal.vue';
import Card from './Card.vue' ;
export default {
  name: 'App',
  data(){
    return{
      오프젝트 : { name : 'kim' , age :20},
      누른거 : 0,
      원룸들 : data,
      모달창열렸니 : false, 
      신고수 : 0,
      menus : ['Home','Shop','About'],
      products: ['역삼동원룸', '천호동원룸', '마포구원룸'],
    }
  },
  components: { 
    Discount, //등록
    Modal,
    Card,
  }
}
</script>

<style>
.discount {
  background: #eee;
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
}
body {
  margin : 0
}
div {
  box-sizinga: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
.room-img{
  width: 50%;
  margin-top: 40px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}

.menu {
  background: darkslateblue;
  padding: 15px;
  bordor-radius:5px;
}
.menu a {
color: white;
padding: 10px;
}

</style>
