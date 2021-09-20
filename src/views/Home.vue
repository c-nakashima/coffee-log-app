<template>
  <v-app>
    <v-content class="pa-0">
      <div class="container">
        <coffee-store-card />
      </div>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "../components/HelloWorld";
import CoffeeStoreCard from "../components/CoffeeStoreCard";

export default {
  name: "Home",

  components: {
    HelloWorld,
    CoffeeStoreCard,
  },
};
</script>

<style scoped>
.container {
  background-color: aquamarine;
}
</style>