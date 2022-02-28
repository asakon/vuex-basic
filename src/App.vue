<template>
  <div id="app">
    <input type="button" value="-" v-on:click="minus">
    カウント：{{count}}
    <input type="button" value="+" v-on:click="plus">
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'App',
  computed: mapState([ 'count']),
  methods: {
    minus() {
      this.$store.commit('minus');
    },
    plus() {
      this.$store.commit('plus')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
