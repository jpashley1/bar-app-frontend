<script>
export default {
  props: {
    products: Array,
  },
};


</script>

<template>
  <div>
    <h1>All products</h1>
    <div v-for="product in products" v-bind:key="product.id">
      <h2>{{ product.name }}</h2>
      <!-- <img v-bind:src="product.url" /> -->
      <p>category: {{ product.category }}</p>
      <p>price: {{ product.price }}</p>
    </div>
  </div>
</template>

<style></style>