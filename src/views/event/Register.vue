<script setup>
import { useRouter } from "vue-router";
import { defineProps, inject } from "vue";

const props = defineProps(["event"]);
const router = useRouter();
const GStore = inject("GStore");

const register = () => {
  GStore.flashMessage =
    "You are successfully registered for " + props.event.title;
  setTimeout(() => {
    GStore.flashMessage = "";
  }, 3000);
  router.push({
    name: "EventDetails",
  });
};
</script>

<template>
  <p>Register for the event here</p>
  <button @click="register">Register Me!</button>
</template>
