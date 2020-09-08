<template>
  <div>
    <h1>My Shop</h1>
    <FontAwesomeIcon></FontAwesomeIcon>
    <Navbar
      :cart="cart"
      :cart-qty="cartQty"
      :cart-total="cartTotal"

    ></Navbar>
    <PriceSlider
      :slider-status="sliderStatus"
      :maximum.sync="maximum"
    ></PriceSlider>

    <product-list
      :maximum="maximum"
      :products="products"

    ></product-list>
  </div>
</template>

<script>

import ProductList from "@/components/ProductList.vue";
import PriceSlider from "@/components/PriceSlider.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  name: "Products",
  props: [
    "products",
    "maximum",
    "cart",
    "cartQty",
    "cartTotal",
    "sliderStatus",
    "sliderState"
  ],
  components: {
    Navbar,
    PriceSlider,
    ProductList
  }
};
</script>

<style scoped></style>
