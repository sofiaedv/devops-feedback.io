<script>
import { RouterLink, RouterView } from 'vue-router'
import { routes } from './router';
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
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