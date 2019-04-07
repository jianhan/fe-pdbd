<template>
  <v-app dark id="inspire">
    <LeftNavigationDrawerVue/>
    <v-toolbar color="blue" dense fixed clipped-left app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-icon class="mx-3">fa-youtube</v-icon>
      <v-toolbar-title class="mr-5 align-center">
        <span class="title">PDBD</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-layout row align-center style="max-width: 650px">
        <v-text-field
          placeholder="Search..."
          single-line
          append-icon="search"
          :append-icon-cb="() => {}"
          color="white"
          hide-details
        ></v-text-field>
      </v-layout>
    </v-toolbar>
    <v-content>
      <v-container fill-height>
        <v-layout justify-center align-center></v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import LeftNavigationDrawerVue from './components/LeftNavigationDrawer.vue';

export default {
  name: 'App',
  components: {
    LeftNavigationDrawerVue,
  },
  data: () => ({
    drawer: true,
  }),
  props: {
    source: String,
  },
};
</script>
