<template lang="">
  <h1>Vue Js</h1>
  <!-- Pasar componente -->
  <Card />
</template>
<script>
// Se importa el componente en el script
import Card from "./components/Card.vue";

export default {
  //Y despues se declara el components
  components: {
    Card,
  },
};
</script>
<style lang=""></style>
