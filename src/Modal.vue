<template>
  
<div class="black-bg" v-if="모달창열렸니==true">
  <div class="white-bg">
    <img :src ="원룸들[누른거].image" style ="width=100%">
    <h4>{{ 원룸들[누른거].title }}</h4>
    <p>{{원룸들[누른거].content}}</p>
    <p>가격 : {{원룸들[누른거].price}} 만원</p>
    <!-- <button @click="모달창열렸니=false">닫기</button> -->
  </div>
</div>
</template>

<script>
export default {
    props : { //props 2번 등록 
        원룸들 : Array,
        누른거 : Number,
        모달창열렸니 : Boolean,
    }
}
</script>

<style>

</style>