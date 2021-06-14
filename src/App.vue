<template>
  <v-app>
    <v-app-bar app color="primary" dark> Mario Logistics </v-app-bar>
    <login />
  </v-app>
</template>

<script>
import Login from "./components/Login.vue";

export default {
  name: "App",

  components: {
    Login,
  },

  data: () => ({
    //
  }),
};
</script>
