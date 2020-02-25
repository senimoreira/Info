<template>
  <div id="app">
    <Information/>
  </div>
</template>

<script>
import Information from './components/Information.vue'

export default {
  name: 'App',
  components: {
    Information
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-left: 60px;
}
</style>
