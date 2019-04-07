<template>
  <v-navigation-drawer fixed clipped v-model="drawer" app>
    <v-list dense>
      <!-- main navigation links -->
      <v-list-tile v-for="link in links" :key="link.text" @click="alert('test')">
        <v-list-tile-action>
          <v-icon>{{ link.icon }}</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>{{ link.text }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-subheader class="mt-3 grey--text text--darken-1">SUBSCRIPTIONS</v-subheader>

      <!-- configuration links -->
      <v-list-tile class="mt-3" @click="alert('test')">
        <v-list-tile-action>
          <v-icon color="grey darken-1">add_circle_outline</v-icon>
        </v-list-tile-action>
        <v-list-tile-title class="grey--text text--darken-1">Browse Channels</v-list-tile-title>
      </v-list-tile>
      <v-list-tile @click="alert('test')">
        <v-list-tile-action>
          <v-icon color="grey darken-1">settings</v-icon>
        </v-list-tile-action>
        <v-list-tile-title class="grey--text text--darken-1">Manage Subscriptions</v-list-tile-title>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    drawer: true,
    links: [
      { icon: 'trending_up', text: 'Most Popular' },
      { icon: 'subscriptions', text: 'Subscriptions' },
      { icon: 'history', text: 'History' },
      { icon: 'featured_play_list', text: 'Playlists' },
      { icon: 'watch_later', text: 'Watch Later' },
    ],
  }),
};
</script>
