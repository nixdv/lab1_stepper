<template>
  <v-app>
    <v-main>
      <Stepper1/>
    </v-main>
  </v-app>
</template>

<script>
import Stepper1 from './components/Stepper.vue'
export default {
  name: 'App',
  components: {
    Stepper1
  }
}
</script>

<style>
#app {
  font-family: Avenir, San Francisco, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 60px;
}
</style>
