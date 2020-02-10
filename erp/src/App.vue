<template>
  <div id="app">
    <Caixa/>
  </div>
</template>

<script>



import Caixa from './components/caixa'

export default {
  name: 'App',
  components: {
      Caixa,
  }
}
</script>

<style>

/* @import 'assets/_bootstrap.scss';
@import url('_variables.scss'); */

body{
  background: rgb(2,0,36);
background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(9,9,121,1) 53%, rgba(0,212,255,1) 100%);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
