<template>
  <div class="product-item">
            <img :src="product.imageUrl" alt="">
            <h3 class="product-name">{{ product.name }}</h3>
            <p class="product-price">Rp{{ product.price }}</p>
            <router-link :to="{ name : 'productDetail', params: {id: product.id} }">
              <button>Detail</button>
            </router-link>
            
        </div>
</template>

<script>
export default {
    props: [
        'product'
    ]
}
</script>

<style scoped>
  .product-item {
    align-items: center;
    border-radius: 10px;
    box-shadow: 0px 2px 5px #888;
    display: flex;
    flex-direction: column;
    margin-bottom: 5%;
    padding: 20px;
    position: relative;
    width: 32%;
  }

  .product-name {
    margin-bottom: 5px;
  }

  img {
    height: 230px;
    width: 230px;
    border-radius: 5%;
    justify-content: auto;
  }

  a {
    width: 100%;
  }

  button {
    width: 95%;
    margin-bottom: 20px;
  }
</style>