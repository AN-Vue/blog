<template>
    <div class="modal-root">
        <h1>Teleport Example component</h1>
      <button @click="showModal = true">Open Modal</button>
        <div v-if="showModal" class="modal">
          <p>This modal is teleported to #modal-root!</p>
          <button @click="showModal = false">Close Modal</button>
        </div>
    </div>
  </template>
  
<script>
  export default {
    name: 'TeleportExample',
    data() {
      return {
        showModal: false,
      };
    },
  };
</script>
  
<style>
  .modal {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
</style>