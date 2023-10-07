<template>
  <div>
    <header>
      <h1>Bienvenido a la Landing Page de Vue 3</h1>
    </header>
    <section>
      <div v-if="showIntroduction">
        <h2>Introducción a Vue 3</h2>
        <p>Vue 3 es un framework progresivo para la creación de interfaces de usuario. Ofrece muchas características poderosas y flexibles para desarrolladores web.</p>
      </div>
    </section>
    <section>
      <div v-if="showIntroduction">
        <h2>Que es</h2>
        <p>Como desarrolladores front-end, generalmente queremos elegir la tecnología más adecuada para cada uno de nuestros proyectos con el fin de mejorar la forma en que escribimos y organizamos el código. Por lo tanto, el objetivo principal de este artículo es revisar las características principales de Vue.js, un marco de JavaScript progresivo, que nos permite desarrollar rápidamente aplicaciones de una sola página (SPA) que se mantienen fácilmente mientras se utilizan sus componentes y características reactivas, como como interfaces reactivas y enlace de datos.</p>
      </div>
    </section>
    <section>
      <div v-if="showIntroduction">
        <h2>Historia</h2>
        <p>Vue fue creado por Evan You después de trabajar para Google usando AngularJS en varios proyectos. Más tarde resumió su proceso de pensamiento: "Pensé, ¿qué tal si pudiera extraer la parte que realmente me gustaba de Angular y construir algo realmente liviano?"8​ El primer código fuente comprometido con el proyecto fue fechado en julio de 2013, y Vue fue liberado por primera vez en febrero siguiente, en 2014.

        </p>
      </div>
    </section>
    <features-list :features="features"></features-list>
    <section>
      <div :class="{'highlighted': isHighlighted}">
        <h2>¡Aprende y disfruta Vue 3!</h2>
      </div>
    </section>
  </div>
</template>

<script>
import FeaturesList from "@/components/mines/FeatureList.vue"; // Ajusta la ruta según tu estructura de archivos

export default {
  components: {
    FeaturesList
  },
  data() {
    return {
      showIntroduction: true,
      features: [
        { id: 1, title: 'Reactividad con el sistema de reactividad de Vue', description: 'Vue 3 utiliza un sistema de reactividad eficiente para actualizar automáticamente la interfaz de usuario.' },
        { id: 2, title: 'Componentes reutilizables', description: 'Puedes crear componentes reutilizables en Vue para construir interfaces de usuario modulares.' },
        { id: 3, title: 'Directivas poderosas', description: 'Vue ofrece directivas como v-if, v-for y v-bind para facilitar la manipulación del DOM.' },
        { id: 4, title: 'Enrutamiento con Vue Router', description: 'Vue Router permite crear aplicaciones de una sola página (SPA) con enrutamiento.' },
        { id: 5, title: 'Gestión de estado con Vuex', description: 'Vuex es una biblioteca que simplifica la gestión del estado de la aplicación en Vue.' },
      ],
      isHighlighted: true
    };
  }
};
</script>

<style scoped>
/* Estilos opcionales aquí */
</style>
