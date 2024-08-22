<template>
  <div>
    <h1>Simple Todo List</h1>
    <input
      v-model="newTodo"
      @keyup.enter="addTodo"
      placeholder="Add a new todo"
    />
    <button @click="addTodo">Add</button>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        {{ todo }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TodoList",
  data() {
    return {
      newTodo: "",
      todos: [] as string[],
    };
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim()) {
        this.todos.push(this.newTodo);
        this.newTodo = "";
      }
    },
  },
});
</script>

<style scoped>
div {
  margin-top: 20px;
}
</style>
