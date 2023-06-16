<script setup>
import { ref, computed } from 'vue';

// Iteration 1
const resultado = computed(() => {
  return 2 + 2;
});

// Iteration 2
const nombre = ref('Chloe');
const edad = ref(29);
const obtenerCadena = () => {
  return `Hola, mi nombre es ${nombre.value} y tengo ${edad.value} años.`;
};

// Iteration 3
const mostrarElemento = ref(false);

// Iteration 4
const publicaciones = ref([
  {
    id: 1,
    titulo: 'Publicación 1',
    descripcion: 'Descripción de la publicación 1',
    contenido: 'Contenido de la publicación 1'
  },
  {
    id: 2,
    titulo: 'Publicación 2',
    descripcion: 'Descripción de la publicación 2',
    contenido: 'Contenido de la publicación 2'
  },
  {
    id: 3,
    titulo: 'Publicación 3',
    descripcion: 'Descripción de la publicación 3',
    contenido: 'Contenido de la publicación 3'
  }
]);
</script>

<template>
  <div>
    <h1>LAB | Fundamentos de Vue.js</h1>
    <br>
    <h2>Iteración 1.</h2>
    <div>
      <p>El resultado es: {{ resultado }}</p>
    </div>

    <h2>Iteración 2.</h2>
    <div>
      <p>{{ obtenerCadena() }}</p>
    </div>

    <h2>Iteración 3.</h2>
    <div>
      <p v-if="mostrarElemento">Hola, el elemento es True!!!</p>
      <p v-else>Hola, el elemento es falso!!! Si fuese true se mostraría otro mensaje!!!</p>
    </div>

    <h2>Iteración 4.</h2>
    <div>
      <h3>Lista de Publicaciones:</h3>
      <ul>
        <li v-for="publicacion in publicaciones" :key="publicacion.id">
          <h3>{{ publicacion.titulo }}</h3>
          <p>{{ publicacion.descripcion }}</p>
          <p>{{ publicacion.contenido }}</p>
        </li>
      </ul>
    </div>
    <br>
  </div>
</template>

<style scoped>
/* Estilo del botón */
.boton {
  background-color: greenyellow;
  width: 100px;
  height: 50px;
  border-radius: 20px;
  margin-bottom: 20px;
  margin-left: 50px;
}

.style {
  width: 350px;
  margin-left: 10px;
  border-radius: 20px;
  margin-bottom: 20px;
}
</style>
