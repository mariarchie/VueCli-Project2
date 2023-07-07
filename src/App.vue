<template>
  <div id="app">
    <PageHeader />
    <div class="product-container center">
      <div v-for="product in products" :key="product.name">
        <product-details :product="product"></product-details>
      </div>
    </div>
    <PageFooter />
  </div>
</template>
  
<script>
import PageHeader from './components/PageHeader.vue';
import ProductDetails from './components/ProductDetails.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'App',
  components: {
    PageHeader,
    ProductDetails,
    PageFooter,
  },
  data() {
    return {
      products: [
        {
          name: 'Product 1',
          price: 17.05,
          available: true
        },
        {
          name: 'Product 2',
          price: 2029.99,
          available: false
        },
        {
          name: 'Product 3',
          price: 589.00,
          available: true
        }
      ]
    };
  }
};
</script>


<style lang="scss">
@import "@/styles/style.scss";
</style>