<template>
  <h2>Home Page</h2>
  <NuxtLink to="/about" class="routeclass">About</NuxtLink>
    <div v-if="pending">
        Loading ...
    </div>
  <ul>
      <li v-for="user in users" :key="user.id"> {{ user.name }}</li>
  </ul>
</template>

<script setup>
  const  { pending, data: users } = await useLazyFetch('https://jsonplaceholder.typicode.com/users');
</script>

<style scoped>
  .routeclass {
    color: red;
  }
</style>