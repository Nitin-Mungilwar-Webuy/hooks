<script setup>
import {
  ref,
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";

onBeforeMount(() => {
  console.log("onBeforeMount called-child");
});
onMounted(() => {
  console.log("onMounted called-child");
});
onBeforeUpdate(() => {
  console.log("onBeforeUpdate called-child");
});
onUpdated(() => {
  console.log("onUpdated called-child");
});
onBeforeUnmount(() => {
  console.log("onBeforeUnmount called-child");
});
onUnmounted(() => {
  console.log("onUnmounted called-child");
});
</script>
<template><h1>hello component child</h1></template>
<style></style>
