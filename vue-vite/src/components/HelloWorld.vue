<script setup lang="ts">
import { ref } from 'vue'
defineProps<{msg?: string}>()

// me falta gran parte del desarrollo del TP, lo que respecta una de las clases que falte y no quedo grabada, asi que estoy medio a oscuras.
const nombre = ref("");
const email = ref("");
const contrasenha = ref("");
const nacimiento = ref("");

function guardarDatos() {
  if (nombre.value && email.value && contrasenha.value && nacimiento.value) {
    nombre.value = "";
    email.value = "";
    contrasenha.value = "";
    nacimiento.value = "";
  } else {
    alert("Se deben completar los datos requeridos");
  }
}
</script>

<template>
  <h2>{{ msg }}</h2>
  <input type="text" placeholder="Nombre de Usuario" v-model="nombre">
  <input type="email" placeholder="Email" v-model="email">
  <input type="password" placeholder="Contraseña" v-model="contrasenha">
  <input type="date" placeholder="Fecha de Nacimiento" v-model="nacimiento">
  <button @click="guardarDatos">Guardar</button>
</template>
