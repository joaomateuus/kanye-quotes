<template>
    <div>

    </div>
</template>

<script>
import axios from 'axios';
import { onMounted } from '@vue/runtime-core';

export default {

  components: {},
  setup() {
    const quotes = '';

    onMounted (()=>{
      try {
        axios.get('https://api.kanye.rest/').then((response) => {
          console.log(response);
          this.quotes = response.data;
        })  
      } catch (error) {
        console.log(error);
      }
    })

    return{

  }
  
  }
  
  

}


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
