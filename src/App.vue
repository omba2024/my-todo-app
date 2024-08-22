<template>
  <div id="app">
    <TodoList />
  </div>
</template>

<script>
import TodoList from "./components/TodoApp.vue";

export default {
  name: "App",
  components: {
    TodoList,
  },
};
</script>
