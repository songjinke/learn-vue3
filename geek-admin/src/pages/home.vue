<template>
  <h1>这是首页</h1>
  <Count/>
  <TodoList/>
</template>

<script setup>
import TodoList from '../components/TodoList.vue'
import Count from '../components/Count.vue'
import {useMouse} from '../utils/mouse'

let {x, y} = useMouse()
</script>

<style scoped>
h1 {
  color: red;
}
</style>>