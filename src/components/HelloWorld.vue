<template>
  <h1>{{ name }},{{ age }}</h1>
</template>

<script setup lang="ts">
interface IOpt {
  name: string;
  age: number;
}

// if use import interface from url ,error:
// import type { IOpt } from "./types";
const props = withDefaults(defineProps<IOpt>(), {
  name: "xx",
  age: 2,
});
</script>
