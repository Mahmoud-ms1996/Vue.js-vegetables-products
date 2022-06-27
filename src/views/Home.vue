<template>
  <div class="home">
    <div class="splash-container">
        <div class="splash">
          <h1>Splendid Food</h1>
        </div>
      </div>

    <main class="wrapper">

      <h2>Recommended</h2>

      <div class="recommended">

        <ProductCard
          class="card"
          v-for="(product, index) in inventory.slice(0,3)"
          :key="product.id"
          :index="index"
          :product="product"
          :addToCart="addToCart"
        />

      </div>

    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductCard from '@/components/product-card.vue'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>
