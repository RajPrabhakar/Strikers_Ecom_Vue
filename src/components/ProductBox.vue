<template>
    <div class="column is-2">
        <div class="box">
        <figure class="image mb-4 is-1by1">
            <img :src="product.get_thumbnail">
        </figure>

        <h3 class="is-size-4">{{ product.name }}</h3>
        <p class="is_size-6 has-text-grey">INR {{ product.price }}</p>
        <router-link v-bind:to="product.get_absolute_url" class="button is-dark mt-4">View details</router-link>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductBox',
    props: {
        product: Object
    }
}
</script>

<style scoped>
  .image {
    margin-top: -1.25rem;
    margin-left: -1.25rem;
    margin-right: -1.25rem;
  }
  img {
    object-fit: contain;
  }
</style>