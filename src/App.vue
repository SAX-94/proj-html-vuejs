<template>
  <div id="app">
    <TheHeader></TheHeader>
    <MainComponent></MainComponent>
    <TheFooter></TheFooter>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import MainComponent from './components/MainComponent.vue'
import TheFooter from './components/TheFooter.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    MainComponent,
    TheFooter
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400;600;700;800;900&display=swap');
#app {
  font-family: 'Nunito', sans-serif;
}
</style>
