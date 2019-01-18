<template>
  <div>
    <input v-model="todoItem" type="text">
    <button v-on:click="addTodoItem">Submit</button>
    <ol>
      <li v-for="(todoItem,i) in todoItems" :key="todoItem">
        {{todoItem}}
        <button></button>
      </li>
    </ol>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class TodoList extends Vue {
  todoItem: string = "";
  todoItems: string[] = [];
  message: string = "Item Succesfully added!";
  addTodoItem() {
    this.todoItems.push(this.todoItem);
    this.todoItem = "";
    this.itemAddedMessage();
  }
  itemAddedMessage() {
    alert(this.message);
  }

  removeTodoListItem(index: number) {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
