<template>
  <div>
    <div class="card card-compact bg-base-100 h-96 shadow-xl">
      <figure>
        <img :src="product.image" class="image-full overflow-hidden" />
      </figure>
      <div class="card-body">
        <h2 class="card-title">{{ product.title }}</h2>

        <p>If a dog chews shoes, whose shoes does he choose?</p>
        <div class="card-actions justify-end">
          <button class="btn btn-primary">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
console.log(product.title);
</script>

<style scoped></style>
