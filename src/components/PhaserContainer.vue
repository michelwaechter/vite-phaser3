<script setup>
import { onMounted, onUnmounted } from 'vue'
const props = defineProps({
  containerID: {
    type: String,
    default: 'game-container'
  }
});
let gameInstance = null
const containerId = 'game-container'
const game = await import(/* webpackChunkName: "game" */ '@/game/game')

onMounted(() => {
  gameInstance = game.launch(containerId)
})

onUnmounted(() => {
  gameInstance.destroy(false)
})
</script>

<template>
  <div :id="containerId" />
</template>
