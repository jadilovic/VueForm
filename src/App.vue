<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <AddressFieldGroupVue msg="Vue Form" label="Address" v-model="streetName" />
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import AddressFieldGroupVue from './components/AddressFieldGroup.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    AddressFieldGroupVue
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
