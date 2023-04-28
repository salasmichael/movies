<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    
    <h1 class="title">Tecno Movies</h1>

    <RouterView />
  </div>
</template>

<style scoped>
.layout {
  width: 1200px;
  max-width: 100%;
  margin-left: auto;
  margin-right: auto;
  padding: 40px 20px;
}
.title {
  text-align: center;
  color: var(--color-primary);
  font-size: 40px;
  font-weight: 700;
  margin-bottom: calc(var(--spacing) * 3);
}
</style>