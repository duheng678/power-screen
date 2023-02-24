<template>
  <RouterView />
</template>

<script setup>
import { RouterView } from "vue-router";
import useScalePage from "@/hooks";
useScalePage();
</script>
<style scoped></style>
