<script setup>
import { ref } from 'vue'
const count = ref(0)

const  Increment = () => {
  if(count.value >= 10){
    count.value = 0
  }
  count.value++
}


const Decrement = () => {
  if(count.value <= 0){
    count.value = 10
  }
  count.value--
}

</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="Increment">Increment</button>
  <button @click="Decrement">Decrement</button>
</template>
