<template>
  <site-nav></site-nav>
  <main>
    <router-view />
  </main>
</template>
<script setup>
import SiteNav from '@/components/site-nav/index.vue'
</script>

<style lang="scss">
.app {
  color: red;
}
</style>