<script setup>
import { ref } from 'vue'

// import HelloWorld from './components/HelloWorld.vue'
import IconEyeSlash from './components/IconEyeSlash.vue';
import IconTelegram from './components/IconTelegram.vue'
import IconUnlock from './components/IconUnlock.vue'
import IconUser from './components/IconUser.vue'
import IconX from './components/IconX.vue'
import IconMagnifyingGlass from './components/IconMagnifyingGlass.vue'
import IconArrowDeg from './components/IconArrowDeg.vue'
import IconUsers from './components/IconUsers.vue'
import IconLayers from './components/IconLayers.vue'
import IconFourSquare from './components/IconFourSquare.vue'
import IconFolder from './components/IconFolder.vue'

const arrowAngle = ref(0)

function handleIncrementArrowAngle() {
  arrowAngle.value += 10
}
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 1em;">
    <IconEyeSlash style="color: green" />
    <IconTelegram style="color: magenta" />
    <IconUnlock style="color: blue" />
    <IconUser style="color: orange" />
    <IconX style="color: red" />
    <IconMagnifyingGlass style="color: magenta" />
    <IconArrowDeg :angle="arrowAngle" />
    <IconUsers />
    <IconLayers />
    <IconFourSquare />
    <IconFolder />

    <button
      @click="handleIncrementArrowAngle"
      class="py-2 bg-stone-700 rounded-lg"
    >arrowAngle ++</button>
  </div>
</template>
