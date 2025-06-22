<script setup>
import { defineProps } from "vue";
const props = defineProps({
  value: Object,
});
console.log(props.value);
</script>

<template>
  <div class="flex flex-col w-full bg-gray-50">
    <div class="flex">
      <div class="mr-1" v-for="tag in value.tags" :key="tag.id">
        {{ tag.title }}
      </div>
    </div>
    <div class="grid grid-cols-5 gap-x-0.5 py-1">
      <p class="col-span-4 text-left">{{ value.title }}</p>
      <p class="col-span-1 text-right">{{ value.createdAt }}</p>
    </div>
    <div class="text-left">{{ value.content }}</div>
    <p class="text-left pt-3">{{ value.author }}</p>
  </div>
</template>