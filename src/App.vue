<template>
  <div id="app">
    <Header />
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Header from './components/layout/Header'
import Todos from './components/Todos'
import AddTodo from './components/AddTodo'

export default {
  name: 'app',
  components: {
    AddTodo,
    Header,
    Todos
  },
  data() {
      return {
          todos: []
      }
  },
  methods: {
      deleteTodo(id) {
          this.todos = this.todos.filter(todo => todo.id !== id);
      },
      addTodo(newTodo) {
          this.todos = [...this.todos, newTodo]
      }
  },
  created() {

  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
    background: #555555;
    color: #ffffff;
    padding: 7px 20px;
    cursor: pointer;
  }
</style>
