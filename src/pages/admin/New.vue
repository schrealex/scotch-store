<template>
  <product-form
    :manufacturers="manufacturers"
    :model="model"
    @save-product="addProduct">
  </product-form>
</template>

<script>
import ProductFrom from '@/components/product/ProductForm';

export default {
  data() {
    return {
      model: {},
      manufacturers: [
        {
          _id: 'sam',
          name: 'Samsung',
        },
        {
          _id: 'apple',
          name: 'Apple',
        },
      ],
    };
  },
  methods: {
    addProduct(model) {
      console.log('model', model);
    },
  },
  components: {
    'product-form': ProductFrom,
  },
};
</script>
