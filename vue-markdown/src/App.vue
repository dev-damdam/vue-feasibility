<template>
  <div id="app">
    <markdown-sample />
  </div>
</template>

<script>
import MarkdownSample from "./components/markdown-sample.vue";

export default {
  name: "App",
  components: {
    MarkdownSample,
  },
};
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
