<script setup>
import { ref } from "vue";

const isOpen = ref(false);

function openModal() {
  isOpen.value = true;
}

function closeModal() {
  isOpen.value = false;
}
</script>

<template>
  <div>
    <button class="btn" @click="openModal">
      Subscribe
    </button>

    <div v-if="isOpen" class="overlay">
      <div class="modal">
        <h2>Join InsightAI</h2>
        <p>Get early access to our platform.</p>
        <input placeholder="Your email" />
        <button class="btn" @click="closeModal">Submit</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.btn {
  background: #3b82f6;
  color: white;
  border: none;
  padding: 0.7rem 1.3rem;
  border-radius: 9999px;
  cursor: pointer;
  font-weight: 600;
  transition: transform 0.2s;
}

.btn:hover {
  transform: translateY(-2px);
  background: #2563eb;
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  backdrop-filter: blur(4px);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal {
  background: rgba(15, 23, 42, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.1);
  color: white;
  padding: 2rem;
  border-radius: 24px;
  width: 320px;
  text-align: center;
  box-shadow: 0 20px 50px -10px rgba(0, 0, 0, 0.5);
  backdrop-filter: blur(12px);
}

.modal h2 {
  margin-top: 0;
}

.modal p {
  color: #94a3b8;
}

input {
  width: 100%;
  padding: 0.8rem;
  margin: 1rem 0;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  background: rgba(0, 0, 0, 0.3);
  color: white;
  outline: none;
}

input:focus {
  border-color: #3b82f6;
}
</style>
