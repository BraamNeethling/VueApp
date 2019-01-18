<template>
  <div>
    <h1>Todo List</h1>
    <TodoList/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoList from '@/components/TodoList.vue'; // @ is an alias to /src

@Component({
  components: {
    TodoList,
  },
})
export default class Todo extends Vue {}
</script>
