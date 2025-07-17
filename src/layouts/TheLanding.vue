<script setup lang="ts">
import TheHeader from '@/components/TheHeader.vue'
import TheFooter from '@/components/TheFooter.vue'
</script>

<template>
    <TheHeader></TheHeader>
    <main><slot></slot></main>
    <TheFooter></TheFooter>
</template>

<style scoped></style>
