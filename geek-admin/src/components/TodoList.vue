<template>
  <div>
    <input v-model="title" type="text" @keydown.enter="addTodo"/>
    <button v-if="active < all" @click="clear">清理</button>
    <ul v-if="todos.length">
      <li v-for="todo in todos">
        <input v-model="todo.done" type="checkbox"/>
        <span :class="{ done: todo.done }"> {{ todo.title }}</span>
      </li>
    </ul>
    <div v-else>暂无数据</div>
    <div>
      全选<input v-model="allDone" type="checkbox"/>
      <span> {{ active }} / {{ all }} </span>
    </div>
  </div>
</template>

<script setup>
import useTodos from '../utils/useTodos'

let {title, todos, addTodo, clear, active, all, allDone} = useTodos();
</script>