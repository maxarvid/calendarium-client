<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'

const drawer = ref(false)

</script>

<template>
  <v-app>
    <v-navigation-drawer v-model="drawer">
      <v-list>
        <v-list-item>
          <RouterLink to="/">Home</RouterLink>
        </v-list-item>
        <v-list-item>
          <RouterLink to="/about">About</RouterLink>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="() => drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Calendarium</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <RouterView />
    </v-main>
  </v-app>
</template>

<style scoped></style>
