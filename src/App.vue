<script>
import { RouterLink, RouterView } from 'vue-router';
import { routes } from './router';

export default {
  name: 'App',
  data() {
    return {
      routes
    };
  },
  methods: {
    formatRouteName(name) {
      // Capitalize the first letter for display in the navigation bar
      return name.charAt(0).toUpperCase() + name.slice(1);
    }
  }
};
</script>

<template>
  <div>
    <nav>
      <RouterLink
        v-for="route in routes"
        :key="route.path"
        :to="route.path"
      >
        {{ formatRouteName(route.name) }}
      </RouterLink>
    </nav>
    <RouterView />
  </div>
</template>