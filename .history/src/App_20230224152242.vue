<template>
  <RouterView />
</template>

<script setup>
import { onMounted, onUnmounted } from "vue";
import _ from "lodash";
import { RouterView } from "vue-router";

const resizeFunc = _.throttle(triggerScale, 100);
onMounted(() => {
  triggerScale();
  window.addEventListener("resize", resizeFunc);
});
onUnmounted(() => {
  window.removeEventListener("resize", resizeFunc);
});
</script>
<style scoped></style>
