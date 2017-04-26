<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <input v-model='message' />
    
    <br>
    <a v-bind:href="url"> Click Me</a>
    <p v-if="show">Show Me</p>
    <p v-else="show">Thise is the else</p>
    <ul>
      <li v-for="item in items">{{item.test}}</li>
    </ul>
    <button v-on:click="pressed">Press Me</button>
    <button v-on:click="pressed2">Press Me Twice</button>
    <br>
    <img src="./assets/logo.png">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      message: 'Hello world from chiehwen.',
      url: 'http://www.sina.com.cn',
      show: false,
      items: [
        {test: 123},
        {test2: 456},
        {test: 789}
      ]
    }
  },
  methods: {
    pressed() {
      alert('You Pressed Me!')
    },
    pressed2: function() {
      alert('You Pressed Me Twice.')
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
