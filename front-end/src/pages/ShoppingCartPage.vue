<template>
  <h1>Shopping Cart</h1>
  <ShoppingCartList :cartItems="cartItems" />
</template>

<script>
import { cartItems } from "../temp-data";
import ShoppingCartList from "../components/ShoppingCartList.vue";
export default {
  name: "ShoppingCartPage",
  components: {
    ShoppingCartList,
  },
  data() {
    return {
      cartItems,
    };
  },
};
</script>
