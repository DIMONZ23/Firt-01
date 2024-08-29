<script setup>
const message = 'Hello im Dimonz!'
const rawHtml = '<span style="color:red;">Im so sorry!</span>'
const buttonId = 'button-id'
const buttonClass = 'button-class-rounded'
const isButtonDisabled = false
const objectOfAttrs = {
  id: 'container-id',
  class: 'wrapper-class',
  style: {
    color: 'red'
  }
}
const number = 2;
const listString = 'a,b,c,d,e,f';
const convertToId = (data) => data.split(',').reverse().join('-')
</script>

<template>
  <h1 class="center-text">Syntax</h1>
  <p>Message: {{ message }}</p>
  <span v-html="rawHtml"></span>
  <button :id="buttonId" :class="buttonClass" :disabled="isButtonDisabled">{{isButtonDisabled?'Disable':'Click Here'}}</button>
  <button v-bind="objectOfAttrs">Click now</button>
  <button :id="convertToId(listString)"> Number:{{ number *2 }}</button>
  
</template>
<style>
.center-text {
  text-align: center;
  color: aquamarine;
}
</style>
