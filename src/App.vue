<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
    <div @click="clickPushPaeams">{{ message }}</div>
    <br>
    <router-link v-bind:to = "{ path: '/'}" tag = "span">Router 1</router-link>
    <router-link v-bind:to = "{ path: '/home'}" tag = "span">Router 2</router-link>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    clickPushPaeams: function() {
      this.$router.push({
        name: 'HelloWorld',
        // params: {}
      })
    }
  },
  data () {
    return {
      message: '点击'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
