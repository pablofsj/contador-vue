<template>
  <div id="app">
    <Contador/>
  </div>
</template>

<script>
import Contador from './components/Contador.vue'

export default {
  name: 'App',
  components: {
    Contador
  }
}
</script>

<style>
#app {
  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
