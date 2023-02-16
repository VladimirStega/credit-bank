<template>
  <HelloWorld />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
#app {
  background: #0E0E0E;
}

* {
    box-sizing: border-box;
    padding: 0; 
  }
  
html {
  font-family: 'Geometria', sans-serif;
  background: #0E0E0E;
}
</style>
