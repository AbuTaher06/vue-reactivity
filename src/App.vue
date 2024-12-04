<script setup>
import { ref ,reactive} from 'vue'
const theme=reactive({
  color:"red",
  textColor:"white",
  textSize:"26"
})
// const color=ref("green")
// const textColor=ref("white")
// const textSize=ref("26")
</script>
<template>
  <button class="btn font-bold py-2 px-4 rounded pr-4 space-x-2"
  :class="[
  `text-${theme.textColor}-500 hover:text-${theme.textColor}-700`,
  `bg-${theme.color}-500 hover:bg-${theme.color}-700`]"
  :style="`font-size:${theme.textSize}px`"
  >Click</button>


  <div class="text-red-500 text-2xl my-5">
    <input class="border border-gray-500" type="text" v-model="theme.color" placeholder="Enter Color name" />

    <input class="border border-gray-500 text-2xl" type="text" v-model="theme.textColor" placeholder="Enter your text color" />

    <input class="border border-gray-500 text-2xl" type="text" v-model="theme.textSize" placeholder="Enter your text size" />
  </div>

</template>


<style>

</style>
  

