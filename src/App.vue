<script setup>
import Game from './components/Game.vue';
</script>

<template>
  <div class="flex flex-row">
    <Game />
    <div class="">show you next</div>
  </div>
</template>

<style>
body {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
}

.flex {
  display: flex;
};

.flex-row {
  flex-direction: row;
}
</style>
