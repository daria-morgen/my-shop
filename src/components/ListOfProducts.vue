<template>
  <ul class="listOfProducts">
    <li v-for="(product, index) in products" :key="index" class="product">
      <h2 class="product-name">
        {{ product.name }}
      </h2>
      <div class="product-price">
        <span>R$ {{ product.price }}, 00</span>
<!--        <span>10 x {{ Math.round(product.price / 10) }}, 00 </span>-->
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  props: ['products'],
};
</script>

<style scoped>
.listOfProducts {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 0;
}

.product {
  width: 300px;
  background-color: #fff;
  list-style: none;
  box-sizing: border-box;
  padding: 1em;
  margin: 1em 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 7px;
  /*border-color: black;*/
  border: solid;
}

.product-name {
  font-size: 1.2em;
  font-weight: normal;
}

/*.product-name:hover {*/
/*  cursor: pointer;*/
/*  text-decoration: underline;*/
/*}*/

.product-price {
  width: 100%;
  align-self: flex-start;
  display: flex;
  justify-content: space-between;
  margin-bottom: .5em;
}

</style>

