<script setup>
import { ref } from "vue";
//ref cria dados reativos(dados q mudam durante o processo) mesma lógica do usestate no react
const numero = ref (0);

//função deaumentar
function aumentar () {
  numero.value ++
}

function diminuir () {
 if(numero.value> 0) {
  numero.value --
 }
}
</script>

<template>
  <h1>Contador</h1>
  <h2>{{ numero }}</h2>
   
<!-- pra pegar o evento de click usaremos o v-on ou @ -->
  <button @click="aumentar">+</button>
  <button @click="diminuir">-</button>
</template>

<style >

</style>
