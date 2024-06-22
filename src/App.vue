<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'

const dark_logo = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
</script>

<template>
  <header>
    <img v-if="dark_logo" alt="Vue logo" class="logo" src="@/assets/logo_dark.png" />
    <img v-else alt="Vue logo" class="logo" src="@/assets/logo_light.png" />

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
</style>
