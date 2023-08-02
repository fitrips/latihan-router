<!-- <template>
  <div id="navbar">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
  </div>
  <router-view />
</template> -->

<template>
  <Navbar />
  <router-view />
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components : {
    Navbar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>