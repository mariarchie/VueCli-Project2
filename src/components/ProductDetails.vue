<template>
    <div class="productContent">
        <h3>{{ product.name }}</h3>
        <p>{{ formattedPrice }}</p>
        <p>{{ availability }}</p>
    </div>
</template>
  
<script>
export default {
    props: {
        product: {}
    },
    computed: {
        formattedPrice() {
            const formatted = this.product.price.toFixed(2);
            return '$' + formatted;
        },
        availability() {
            return this.product.available ? 'Available' : 'Out of stock';
        }
    }
};
</script>
  