<template>
  <div id="app">
    <img src="./assets/logo.jpg">
    <Gitops/>
  </div>
</template>

<script>
import Gitops from './components/Gitops'

export default {
  name: 'App',
  components: {
    Gitops
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

.p-float-label {
  display: inline
}
img {
  max-width: 30%
}

</style>
