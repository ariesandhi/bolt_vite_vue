<script setup lang="ts">
import { ref } from 'vue'
import Button from 'primevue/button'

const showLoveMessage = ref(false)
</script>

<template>
  <div class="card">
    <h1>{{ showLoveMessage ? 'I Love You' : 'Hello World!' }}</h1>
    <Button 
      :label="showLoveMessage ? 'Show Hello' : 'Show Love'" 
      @click="showLoveMessage = !showLoveMessage" 
    />
  </div>
</template>

<style scoped>
.card {
  padding: 2rem;
  text-align: center;
}

h1 {
  color: #213547;
  transition: color 0.3s ease;
}

h1:has(+ button:active) {
  color: red;
}
</style>
