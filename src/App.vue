<template>
  <div class="flex flex-col min-h-screen bg-weather-primary">
    <SiteNavigation/>
    <RouterView/>
  </div>
</template>

<script setup>
import SiteNavigation from './components/SiteNavigation.vue';


</script>
