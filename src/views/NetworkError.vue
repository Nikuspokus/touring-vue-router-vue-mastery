<script setup>
defineProps({
  resource: {
    type: String,
    required: true,
    default: "page",
  },
});
</script>

<template>
  <div class="networkError">
    <h1>Uh-Oh!</h1>
    <h3>
      It looks like you're experiencing some network issues, please take a
      breath and <a href="#" @click="$router.go(-1)">click here</a> to try
      again.
    </h3>
    <router-link to="{ name: 'EventList' }">Back to the homepage</router-link>
  </div>
</template>
