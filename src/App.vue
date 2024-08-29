<script setup>
const message = 'Hello im Dimonz!'
const rawHtml = '<span style="color:red;">Im so sorry!</span>'
const buttonId = 'button-id'
const buttonClass = 'button-class-rounded'
const isButtonDisabled = true
const objectOfAttrs = {
  id: 'container-id',
  class: 'wrapper-class',
  style: {
    color: 'red'
  }
}
</script>

<template>
  <h1 class="center-text">Syntax</h1>
  <p>Message: {{ message }}</p>
  <span v-html="rawHtml"></span>
  <button :id="buttonId" :class="buttonClass" :disabled="isButtonDisabled">Click here</button>
  <button v-bind="objectOfAttrs">Click now</button>
</template>
<style>
.center-text {
  text-align: center;
  color: aquamarine;
}
</style>
