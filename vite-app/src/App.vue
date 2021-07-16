<template>
  <router-link to="/">Go to Home</router-link>
  <br />
  <router-link to="/about">Go to About</router-link>
  <br />
  <code> Running on {{ mode }} mode. </code>
  <router-view></router-view>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      mode: location.hostname === "localhost" ? "DEV" : "PROD",
    };
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
