<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <keep-alive>
      <component v-bind:is="component" />
    </keep-alive>
    <button v-on:click="toggle">Toggle</button>
  </div>
</template>
<script>
  import Test from './components/Test.vue'
  import Test2 from './components/Test2.vue'
  export default {
    name: 'app',
    components: {
      Test,
      Test2
    },
    data (){
      return {
        component:"Test2"
      }
    },
    methods: {
      toggle(){
        if (this.component === Test) {
          this.component = Test2;
        } else {
          this.component = Test;
        }
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
