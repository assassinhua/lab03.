<template>
  <div class="event-info">
    <div class="category">{{ event.category }}</div>
    <div class="organizer">{{ event.organizer }}</div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import type { Event } from '@/types'

defineProps<{
  event: Event
}>()
</script>

<style scoped>
.event-info {
  display: flex;
  text-align: center;
  width: 100%;
  padding: 10px;
}

.category,
.organizer {
  font-size: 16px;
  display: inline-block; /* 使元素在行内显示 */
  text-align: right;
  margin-left: 10px; /* 在元素之间添加一些空间 */
}
.organizer {
  margin-right: 0;
}
</style>
