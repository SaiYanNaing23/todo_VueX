<template>
  <div id="app">
    <TodoVue/>
  </div>
</template>

<script>
import TodoVue from './components/Todo.vue';
export default {
  name: 'App',
  components: {TodoVue},
}
</script>