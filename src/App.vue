<template>
  <input type="text" v-model="text">
  <button @click="setText">Sent</button>
  <p v-for="text in textArray" :key="text.message">
  {{text.message}}
  </p>
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
    // textArray
  }
}
</script>

<style>

</style>