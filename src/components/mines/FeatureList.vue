<template>
  <section>
    <h2>Features</h2>
    <ul>
      <li v-for="feature in features" :key="feature.id" @click="toggleFeatureText(feature.id)">
        {{ feature.title }}
        <p v-if="activeFeature === feature.id">{{ feature.description }}</p>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        { id: 1, title: 'Reactividad con el sistema de reactividad de Vue', description: 'Vue 3 utiliza un sistema de reactividad eficiente para actualizar automáticamente la interfaz de usuario.' },
        { id: 2, title: 'Componentes reutilizables', description: 'Puedes crear componentes reutilizables en Vue para construir interfaces de usuario modulares.' },
        { id: 3, title: 'Directivas poderosas', description: 'Vue ofrece directivas como v-if, v-for y v-bind para facilitar la manipulación del DOM.' },
        { id: 4, title: 'Enrutamiento con Vue Router', description: 'Vue Router permite crear aplicaciones de una sola página (SPA) con enrutamiento.' },
        { id: 5, title: 'Gestión de estado con Vuex', description: 'Vuex es una biblioteca que simplifica la gestión del estado de la aplicación en Vue.' },
      ],
      activeFeature: null,
    };
  },
  methods: {
    toggleFeatureText(featureId) {
      this.activeFeature = (this.activeFeature === featureId) ? null : featureId;
    }
  }
};
</script>

<style scoped>
/* Estilos aquí (opcional) */
</style>
