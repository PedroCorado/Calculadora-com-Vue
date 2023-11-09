<template>
  <div id="app">
    <h1>Calculadora Aritmética</h1>
    <Calculadora />
  </div>
</template>

<script>
import Calculadora from "@/Calculadora.vue";

export default {
  name: "App",
  components: {
    Calculadora,
  },
};
</script>
