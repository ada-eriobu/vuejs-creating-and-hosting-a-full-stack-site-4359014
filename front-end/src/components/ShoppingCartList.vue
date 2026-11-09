<template>
  <h1>Shopping Cart</h1>
  <div v-if="cartItems.length > 0">
    <div
      class="product-container"
      v-for="product in cartItems"
      :key="product.id"
    >
      <img :class="product - image" :src="product.imageName" />
      <div class="details-wrap">
        <h3>{{ product.name }}</h3>
        <p>{{ product.price }}</p>
      </div>
      <button class="remove-button">Remove from cart</button>
    </div>
    <button class="checkout-button">Proceed to Checkout</button>
  </div>
  <div v-if="cartItems.length === 0">Your cart is empty</div>
</template>

<script>
export default {
  name: "ShoppingCartList",
  props: ["cartItems"],
};
</script>
