<script setup>
  import {ref} from "vue";

  const count = ref(0);

  const addCount = () => {
    count.value++;
  }

  const subtractCount = () => {
    count.value--;
  }
</script>
  
<!--<script>
  export default({
    data(){
      return{
        count: 0
      }
    },
    methods:{
      addCount(){
        this.count = this.count + 1;
      },
      subtractCount(){
        this.count = this.count -1;
      }
    }
    
  })
</script>
-->

<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{count}}</h1>
      <button @click="subtractCount()">-</button>
      <button @click="addCount()">+</button>
    </div>
  </main>
</template>

<style scoped>
  main{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  h4, h1, p{
    font-size: 60px;
    color: pink;
  }

  button {
    width: 100px;
    height: 50px;
    border: 0;
    border-radius: 50px;
    background-color: pink;
    margin: 10px;
    cursor: pointer;
  }

</style>