<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld :option="temp1" />
  <HelloWorld :option="temp2" />
  <Three />
</template>

<script>
import HelloWorld from './components/MyEchart.vue'
import Three from './components/MyThree.vue'
import { temp1, temp2 } from './mock'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Three
  },
  data() {
    return {
      temp1,
      temp2
    }
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
