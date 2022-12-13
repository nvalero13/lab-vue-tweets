<template>
    <img
      :src="url"
      className="profile"
      alt="profile"
    />
</template>

<script setup>
const props = defineProps(["url"]);
</script>

<style>

</style>