<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <nav-item></nav-item>
    <div>
    <router-view></router-view>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import NavItem from './components/NavItem.vue';
export default {
  name: 'App',
  components: {
    NavItem,
    // HelloWorld
  }
}
</script>

<style>
#app {
  margin: 0;
  padding: 0;
}
</style>
