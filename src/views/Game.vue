<template>
  <h1>This is a Game</h1>
  <p>{{ $route.params.name }}</p>
</template>

<script>
import { useRoute } from "vue-router";
export default {
  name: "Game",
  setup() {
    const route = useRoute();
    console.log(route.params.name);
  },
};
</script>

<style></style>
