<template>
  <div>
    <h1>Filters & Mixins</h1>
    <input v-model="filterText" />
    <ul>
      <li v-for="fruit in filteredFruits" :key="fruit">{{ fruit }}</li>
    </ul>
  </div>
</template>

<script>
import { fruitMixin } from "./fruitMixins";
export default {
  mixins: [fruitMixin],
  created() {
    console.log("Inside List Created Hook");
  },
};
</script>

<style></style>
