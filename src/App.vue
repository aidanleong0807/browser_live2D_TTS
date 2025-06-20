<template>
 <Live2d />
 <AudioPlayer />
</template>

<script setup lang="ts">
import Live2d from "./components/Live2d.vue";
import AudioPlayer from "./components/AudioPlayer.vue";
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
