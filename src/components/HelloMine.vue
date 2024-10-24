<template>
  <div class="father">
    <div v-for="message in list" :key='message'>
      <MyCard :message=message @handleShow="changeList" />
    </div>
  </div>
</template>
<script setup>
import MyCard from './MyCard.vue';
import {ref} from 'vue';
let list=ref(['hello','test','one','two'])
function changeList(message){
  list.value=list.value.filter(item=>item!==message)
  console.log(list)
}
</script>
<style scope>
.father{
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>