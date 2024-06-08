<template>
  <div class="todo-container">
    <h3 class="header">Todo List</h3>
    <div>
      <input class="input-box" type="text" v-model="text">
      <button>add</button>
    </div>
<br>
    <div class="todos" v-for="todo in todos" :key="todos.id">
      <p>{{ todos.text }}</p>
      <input type="checkbox">
      <button>del</button>
    </div>
  </div>
</template>


<script setup>

import { ref } from 'vue';

const text = ref('')
const id = ref(1)

const todos = ref(
  [
    {id: 1, text: 'Wash My Clothes'},
    {id: 1, text: 'Wash My car'},
    {id: 1, text: 'Wash My dog'}
  ]
)
</script>


<style>
.todo-container {
  width: 60%;
  height: 20rem;
  border: 2px solid black;
  margin: 0 auto;
  margin-top: 5%;
}
.header{
  margin-left: 35%;
  margin-top: 10px;
  font-size: 1.3rem;
  font-weight: 600;
}
.input-box{
  width: 60%;
  height: 2rem;
  border: 2px solid black;
  margin-left: 15%;
  margin-right: 5px;
  margin-top: 10px;
}
.todos{
  width: 80%;
  height: 2.5rem;
  border: 2px solid black;
  margin-top: 2rem;
  margin: 0 auto;
  display: flex;
  justify-content: space-evenly;
  align-items: center
}
</style>
