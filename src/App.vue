<template>
<center>
  <HurufGerak/>
  <LoginForm/>
  <HelloWorld/>
</center>
</template>

<script>
import LoginForm from './components/LoginForm.vue'
import HelloWorld from './components/HelloWorld.vue'
import HurufGerak from './components/HurufGerak.vue'

export default {
  name: 'App',
  components: {
    LoginForm,
    HelloWorld,
    HurufGerak
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
