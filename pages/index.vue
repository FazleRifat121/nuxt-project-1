<template>
  <div>
    <banner />
    <NuxtPage />

    <div class="grid grid-cols-3 mt-8 gap-8">
      <div v-for="product in products" :key="product.id">
        <cards :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");

definePageMeta({
  layout: "default",
});
</script>

<style scoped></style>
