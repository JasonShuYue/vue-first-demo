<template>
  <div id="app">

    <TodoItem
        v-for="item in list"
        v-bind:item="item"
        v-on:delete="handleDelete"
    ></TodoItem>
  </div>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
  name: 'app',
  components: {
    TodoItem
  },
  data() {
    return {
      list: ['学习Vue事件', '学习Vue属性', '学习Vue插槽']
    }
  },
  methods: {
    handleDelete(item) {
      const index = this.list.indexOf(item);
      this.list.splice(index, 1);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
