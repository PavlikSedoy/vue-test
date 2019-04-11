<template>
  <div id="app">
    <Todos />
  </div>
</template>

<script>

import Todos from './components/Todos'

export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
      return {
          todos: [
              {
                  id: 1,
                  title: 'Todo One',
                  completed: false
              },
              {
                  id: 2,
                  title: 'Todo Two',
                  completed: false
              },
              {
                  id: 3,
                  title: 'Todo three',
                  completed: false
              },
          ]
      }
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
</style>
