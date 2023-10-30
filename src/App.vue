<template>
  <div id="app">
    <ListJobs />
  </div>
</template>

<script>
import ListJobs from './components/ListJobs'

export default {
  name: 'App',
  components: {
    ListJobs
  }
}
</script>

<style>
#app {
  font-family: "Montserrat","Roboto",sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
