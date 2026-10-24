<script setup lang="ts">
defineProps<{
  name: string
  manaCost: number
  description: string
}>()
</script>

<template>
  <div>
    <p class = "text-orange-500 md:text-green-700">Spell Name: {{ name }}</p>
    <p class = "text-purple-500">Description: {{ description }}</p>
    <p class = "text-pink-500">Mana cost: {{ manaCost }}</p>
    <slot />
  </div>
</template>