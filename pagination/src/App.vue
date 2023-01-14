<template>
  <v-app>
    <v-main>
      <h1>Hello</h1>
      <div class="text-center">
        <v-pagination v-model="page" :length="6"></v-pagination>
      </div>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { ref } from "vue";

export default {
  setup() {
    const page = ref(1);
    const perPage = 12;

    const changePage = () => {
      console.log("Current Page", page.value);
      console.log("Current Docs Required", page.value * perPage);
      console.log("Chaged Again");
    };

    // expose to template and other options API hooks
    return {
      page,
      changePage,
    };
  },
};
</script>
