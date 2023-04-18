<template>
<h2>About Page</h2>
    <NuxtLink to="/">Back To Home</NuxtLink>
</template>

<script setup lang="ts">
definePageMeta({
    pageTransition: {
        name: 'bounce',
        mode: 'out-in' // default
    }
})
</script>