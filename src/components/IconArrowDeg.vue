<script setup>
const props = defineProps({
  angleDeg: {
    type: Number,
    default: 0, // right
  },
  disabled: {
    type: Boolean,
    default: false,
  }
})
</script>

<template>
  <svg 
    xmlns="http://www.w3.org/2000/svg" 
    fill="none" 
    viewBox="0 0 24 24" 
    stroke-width="2" 
    stroke="currentColor"
    :class="{ disabled: disabled }" 
    :style="{ transform: `rotateZ(${angleDeg}deg)` }"
  >
    <path d="M5 12H19" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M12 5L19 12L12 19" stroke-linecap="round" stroke-linejoin="round"/>
  </svg>
</template>

<style scoped>
svg {
  cursor: pointer;
  width: 24px;
}

svg.disabled {
  cursor: default;
  opacity: 0.5;
  pointer-events: none;
}
</style>