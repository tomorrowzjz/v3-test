<template>
  <div v-for="item in arr" :key="item">
    {{ item }}
  </div>
  <button @click="test">test</button>
</template>

<script setup>
import { ref } from 'vue';
let arr = ref(['a','b','c','d','e','f'])
function test() {
  // arr.value = ['d','e','b','c','a','f']
  arr.value = arr.value.reverse()
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
