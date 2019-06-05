<template>
    <div class="todo-item-wrapper">
        <input type="checkbox">
        <span>{{item}}</span>
        <button v-on:click="handleClick">delete</button>
    </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props: ['item'],
    data() {
        return {
            msg: 'hello geek'
        }
    },
    methods: {
        handleClick() {
            this.$emit('delete', this.item);
        }
    }
}
</script>


<style>


</style>
