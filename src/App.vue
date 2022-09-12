<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div class="grid">
    <DefaultCard v-for="card in cards" :key="card.title" :title="card.title" :user="card.user" :list="card.list"/>

  </div>
</template>
<script setup>
  import { ref } from 'vue';
  const cards = ref([
    {
      title: 'DR1',
      user: 'Mikkel Frederiksen',
      list: [
        'Nummer1',
        'Nummer2'
      ]
    },
    {
      title: 'DR2',
      user: 'Mikkel Grøn',
      list: [
        'Nummer1',
        'Nummer2',
        'Nummer3'
      ]
    }
  ])
</script>

<script>
import HelloWorld from './components/HelloWorld.vue';
import DefaultCard from './components/Card.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    DefaultCard
  }
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
