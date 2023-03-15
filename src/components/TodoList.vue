<template>
  <div class="todo-list">
    <div class="todo-item" v-for="todo in todos" :key="todo.id">
      <p>{{ todo.title }}</p>
      <input
        type="checkbox"
        name="todo.id"
        v-on:change="updateTodo(todo)"
        v-bind:checked="todo.completed"
      />
    </div>
    <p>Completed Todos: {{ todosCount }}</p>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      todos: [],
    };
  },
};
</script>