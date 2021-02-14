<template>
  <h1>This is a Game</h1>
  <p>{{ $route.params.name }}</p>

  <button @click="load">Cargar</button>
</template>

<script>
import { useRoute, useRouter } from "vue-router";
export default {
  name: "Game",
  setup() {
    const route = useRoute();
    const router = useRouter();
    console.log(router);

    const load = () => {
      console.log("Ejecutando Petición");
      setTimeout(() => {
        console.log("Volver a la Home");
        router.push("/");
      }, 3000);
    };

    return {
      load,
    };
  },
};
</script>

<style></style>
