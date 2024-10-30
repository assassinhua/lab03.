<script setup lang="ts">
import { toRefs } from 'vue'
import { type Event } from '@/types'
const props = defineProps<{
  event: Event
  id: String
}>()
// eslint-disable-next-line @typescript-eslint/no-unused-vars
import { useRouter } from 'vue-router'
const { event } = toRefs(props)
const router = useRouter()
const register = () => {
  // If the registration API call successful
  // Push back to the event details view
  router.push({ name: 'event-detail-view' })
}

</script>
<template>
  <p>Register event here</p>
  <button @click="register">Register</button>
</template>
