<template>
  <input type="text" v-model="text">
  <button @click="setText">Sent</button>
    <ul v-for="item in textArray" :key="item.message"></ul>
</template>

<script>


export default {
  data(){
    return{
      text:"",
      textArray:[]
      
    }
  },
  methods:{
    setText(){
      this.textArray.push({message: this.text})
    }
  },
  props:{
    textArray
  }
}
</script>

<style>

</style>