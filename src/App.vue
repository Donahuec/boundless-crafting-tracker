<template>
  <v-app>
    <v-app-bar app >
      <v-toolbar-title>Boundless Crafting Tracker</v-toolbar-title>
    </v-app-bar>
    <HelloWorld :recipes="Object.values(json)"/>
    
    <v-footer  app >
      <span class="px-4">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import json from './json/crafting-recipes.json';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data: () => ({
    json: json
  }),
};
</script>
