<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <PasswordReveling v-model="password" id="password" placeholder="Digite sua senha" />
  <br/>
  {{ password }}

</template>

<script>
import PasswordReveling from './components/PasswordReveling.vue'

export default {
  name: 'App',
  components: {
    PasswordReveling
  },
  data() {
    return {
      password: ''
    }
  },
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
