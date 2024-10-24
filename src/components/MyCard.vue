<template>
    <div class="son" @click="handleChange">
      {{ props.message }}
    </div>
</template>
<script setup>
import {defineProps,defineEmits} from 'vue';
const props=defineProps(['message'])
const emit = defineEmits(['handleShow'])

function handleChange(){
  emit('handleShow',props.message)
}
</script>
<style scoped>
.son{
  width: 100px;
  height: 100px;
  background-color:grey;
  border-top:4px solid skyblue;
  border-radius:0 0 12px 12px;
}
</style>