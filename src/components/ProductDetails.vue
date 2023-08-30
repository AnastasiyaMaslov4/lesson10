<template>
  <div class="card">
    <h2>{{ product.name }}</h2>
    <p>Price: {{ formattedPrice }}</p>
    <p v-if="product.available">Available</p>
    <p v-else>Out of stock</p>
  </div>
</template>

<script>
export default {
  name: 'ProductDetails',
  data() {
    return {
      product: {name: 'Product Name', price: 10, available: true},
    }
  },
  computed: {
    formattedPrice() {
      return '$' + this.product.price;
    }
  }
}
</script>

<style scoped lang="scss">
  .card {
    width: 400px;
    border: 1px solid gray;
  }

</style>
