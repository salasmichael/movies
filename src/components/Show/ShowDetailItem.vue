<script setup>
const props = defineProps({
  name: String,
  genres: Array,
  imageSrc: String,
  summary: String
})
</script>

<template>
  <div class="show-detail-item">
    <RouterLink to="/" class="back">&larr; Volver</RouterLink>

    <h1 class="name">{{ props.name }}</h1>
    <p class="genres">Generos: {{ props.genres?.join(', ') }}</p>
    
    <div class="content">
      <img class="cover" :src="props.imageSrc" />
      <div class="summary" v-html="props.summary"></div>
    </div>
  </div>
</template>

<style>
.show-detail-item {
  width: 800px;
  max-width: 100%;
  margin-left: auto;
  margin-right: auto;
}

.back {
  display: block;
  margin-bottom: calc(var(--spacing) * 3);
}
.name{
  color: var(--color-info);
}

.content {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: center;
}

.genres {
  margin-bottom: calc(var(--spacing) * 3);
  color: var(--color-warning);
}

.cover {
  border-radius: 8px;
  margin-bottom: calc(var(--spacing) * 2);
}

.summary p {
  font-size: 20px;
  line-height: 32px;
  color: white;
}

@media screen and (min-width: 900px) {
  .content {
    flex-wrap: nowrap;
    justify-content: flex-start;
  }
  .cover {
    margin-right: calc(var(--spacing) * 3);
  }
}
</style>
