<template>
  <div class="container">
    <h1>QR code generator</h1>

    <sl-input maxlength="255" clearable label="Value" v-model="qrCode"></sl-input>

    <sl-qr-code :value="qrCode"></sl-qr-code>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  import '@shoelace-style/shoelace/dist/components/qr-code/qr-code.js';
  import '@shoelace-style/shoelace/dist/components/input/input.js';

  const qrCode = ref();
</script>

<style>
  .container {
    max-width: 400px;
    margin: 0 auto;
  }

  sl-input {
    margin: var(--sl-spacing-large) 0;
  }
</style>