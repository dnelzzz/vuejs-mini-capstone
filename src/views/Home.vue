<template>
  <div class="home">
    <h1>{{ message }}</h1>
  </div>
</template>

<style></style>

<script>
var axios = require("axios");

export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      products: []
    };
  },
  created: function () {
    axios.get("http://localhost:3000/api/products").then(function (response) {
      this.products = response.data;
    });
  },
  methods: {},
  computed: {}
};
</script>
