<script setup>
import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
  ref,
} from "vue";
import Hello from "./components/Hello.vue";
const showHelloComp = ref(true);
const count = ref(0);

onBeforeMount(() => {
  console.log("onBeforeMount called-parent");
});
onMounted(() => {
  console.log("onMounted called-parent");
});
onBeforeUpdate(() => {
  console.log("onBeforeUpdate called-parent");
});
onUpdated(() => {
  console.log("onUpdated called-parent");
});
onBeforeUnmount(() => {
  console.log("onBeforeUnmount called-parent");
});
onUnmounted(() => {
  console.log("onUnmounted called-parent");
});
</script>

<template>
  <h1>App component parent</h1>
  count: {{ count }}
  <Hello v-if="showHelloComp" />
  <button @click="showHelloComp = !showHelloComp">show/Hide</button>
  <button @click="count++">Increment</button>
</template>

<style scoped></style>
