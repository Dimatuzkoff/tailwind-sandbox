<script setup >
import Card from "./components/Card.vue";
import { boardData } from "./data/board.js";
import { ref } from "vue";

const cardData = boardData[0].groups[0].cards[0];

const card = ref(cardData);
</script>

<template>
  <div class="">
    <Card :value="card"> </Card>
  </div>
</template>

<style>
html,
body,
#app {
  background-color: gray;
}
</style>

