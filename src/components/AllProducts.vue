<template>
  <listOfProducts :products="notebooks"/>
</template>

<script>
import listOfProducts from './ListOfProducts';

export default {
  data() {
    return {
      notebooks: [
        {
          name: 'Notebook Lenovo Ideapad 320 Intel® Core i5-7200u 8GB',
          price: 2259,
          stars: 5,
          totalReviews: 230,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
        {
          name: 'Notebook Dell Inspiron i15-3567-A30P Intel Core 7ª i5 4GB',
          price: 2284,
          stars: 3.4,
          totalReviews: 20,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
        {
          name: 'Notebook Samsung Essentials E21 Intel Celeron Dual Core',
          price: 1490,
          stars: 1,
          totalReviews: 1,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
        {
          name: 'Notebook Samsung Expert X22 Intel Core 7 i5 8GB',
          price: 2307,
          stars: 4.4,
          totalReviews: 340,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
        {
          name: 'Notebook VAIO Fit 15S B1211B Intel Core i5 4GB',
          price: 2599,
          stars: 3,
          totalReviews: 30,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
        {
          name: 'Notebook Dell Alienware - i7 16GB',
          price: 14000,
          stars: 2,
          totalReviews: 248,
          details: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s',
        },
      ]
    }
  },
  components: {
    listOfProducts,
  },
  methods: {
    getList() {
      this.axios.get('http://localhost:8080/getProducts')
          .then(response => (this.info = response));
    }
  }
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
}

.product-name {
  font-size: 1.2em;
  font-weight: normal;
}

.product-price {
  width: 100%;
  align-self: flex-start;
  display: flex;
  justify-content: space-between;
  margin-bottom: .5em;
}

</style>

