<script setup>
import { ref, reactive, isReactive } from 'vue'

const count = ref(0)

const obj = reactive({ a: 1 })

const is_reactive = isReactive(obj)

function updateCount() {
  count.value = 100
}
</script>

<template>
  <div>
    <button @click="updateCount">直接设置 value 为 100</button>
    <button @click="count++">{{ count }}</button>
  </div>
</template>

<style>
button {
  color: red;
}
</style>
