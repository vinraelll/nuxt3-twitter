<template>
  <div class="p-3 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300 border-b" :class="wrappedClasses">
    <slot></slot>
  </div>
</template>

<script setup>
const { defaultTransition, twitterBorderColor } = useTailwindConfig()
const wrappedClasses = computed(() => `${defaultTransition} ${twitterBorderColor}`)
</script>