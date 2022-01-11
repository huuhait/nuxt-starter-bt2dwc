<script setup lang="ts">
const { data } = await useAsyncData('organization', () =>
  $fetch('https://test.zsmartex.tech/api/v2/trade/public/config')
);
</script>

<template>
  <header>
    <h1>{{ data || 'NOW' }}</h1>
  </header>
</template>
