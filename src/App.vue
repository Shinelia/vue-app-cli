<template>
  <div id="app">
    <Welcome />
    <Button class="button" />
    <Button class="button"/>
    <Button class="button button--red"/>
  </div>
</template>

<script>

import Button from './components/Button.vue';
import Welcome from './components/Welcome.vue';

export default {
  name: 'App',
  components: {
    Button,
    Welcome
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
