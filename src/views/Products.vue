<template>
  <main class="wrapper">
        <h1>Products</h1>

        <div class="card-container">
          <ProductCard
            class="card"
            v-for="(product, index) in inventory"
            :key="product.id"
            :index="index"
            :product="product"
            :addToCart="addToCart"
          />
        </div>
      </main>
</template>

<script>
import ProductCard from '@/components/product-card.vue'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Products',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>

<style>
</style>
