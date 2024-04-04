<template lang="">
  <!-- // API DE OPCIONES -->
  <!-- <div>
    <p>Coche</p>
    <p>Marcha: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>color: {{ color[0] }}</p>
    <p>precio: $ {{ price }}</p>
    <p>Poder: {{ power }}</p>
    <p>Mensaje: {{ mensaje.text }}</p>
  </div> -->
  <!-- // COMPOSICION API -->
  <div>
    <p>Coche</p>
    <p>Marcha: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <!-- <p v-for="(color, index) in colors" :key="index">
      color:
      <span> {{ index + 1 }} {{ color }}</span>
    </p>
    <ul>
      <li v-for="(color, index) in colors" :key="index">
        color {{ index + 1 }} : {{ color }}
      </li>
    </ul>
    <p>precio: $ {{ price }}</p>
    <p>Poder: {{ power }}</p>
    <p>Mensaje: {{ mensaje.text }}</p> -->
  </div>
  <div>
    <p>Potencias Urbanas menores a 300</p>
    <ul>
      <!-- renderiza todos -->
      <li v-for="(power, index) in powers" :key="index">
        <template v-if="power < 300">{{ power }}</template>
      </li>
      <!-- renderiza solo los menores a 300 -->
      <template v-for="(power, index) in powers" :key="index">
        <li v-if="power < 300">{{ power }}</li>
      </template>
    </ul>
    <p>Potencias Urbanas mayor a 300</p>
    <ul>
      <template v-for="(power, index) in powers" :key="index">
        <li v-if="power > 299">{{ power }}</li>
      </template>
    </ul>
    <p>Potencias Urbanas Separacion</p>
    <ul>
      <template v-for="(power, index) in powers" :key="index">
        <li v-if="power < 280">Urbana: {{ power }}</li>
        <li v-else-if="power === 280">Hibrida: {{ power }}</li>
        <li v-else>carrera: {{ power }}</li>
      </template>
    </ul>
  </div>
</template>
<script>
export default {
  // API DE OPCIONES
  // data() {
  //   return {
  //     brand: "Audi",
  //     model: "A4",
  //     color: ["azul", "rojo", "verde"],
  //     price: 300000,
  //     power: 180,
  //     mensaje: {
  //       title: "hola mundo",
  //       text: "adios",
  //     },
  //   };
  // },
  // COMPOSICION API
  setup() {
    const brand = "Audi";
    const model = "A4";
    const colors = ["azul", "rojo", "verde"];
    const price = 300000;
    // const power = 180;
    const mensaje = {
      title: "hola mundo",
      text: "adios",
    };
    const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 580];

    return {
      brand,
      model,
      colors,
      price,
      // power,
      mensaje,
      powers,
    };
  },
};
</script>
<style lang=""></style>
