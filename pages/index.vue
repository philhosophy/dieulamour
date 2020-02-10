<template>
  <card class="card"></card>
</template>

<script>
import Card from "~/components/Card.vue"
import Vue from 'vue'

    Vue.prototype.$playSound = (path, volume = 1) => {
      var audio = new Audio(path);
      audio.volume = volume
      audio.play();
}
export default {
  components:{
    Card
  }
}
</script>

<style>
    .card {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}
</style>
