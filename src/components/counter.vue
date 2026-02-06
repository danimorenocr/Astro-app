<script setup>
import { ref } from "vue";

const count = ref(0);
</script>

<template>
  <div class="counter">
    <p>Clicks: {{ count }}</p>
    <button @click="count++">Click me</button>
  </div>
</template>

<style scoped>
.counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

button {
  background: #3b82f6;
  color: white;
  border: none;
  padding: 0.6rem 1.2rem;
  border-radius: 9999px;
  cursor: pointer;
  font-weight: 600;
  transition: background 0.2s;
}

button:hover {
  background: #2563eb;
}

p {
  color: #94a3b8;
  font-weight: 500;
  margin: 0;
}
</style>
