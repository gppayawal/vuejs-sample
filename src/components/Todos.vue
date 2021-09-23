<template>
    <div> <h1> TODO </h1> </div>
    <h3> {{msg}} </h3>
    <p> Hey, creature! Here's your list for today. GLHF! </p>
    <div id="todo-holder">
        <div class="todo-div" v-bind:key="item.id" v-for="item in todos"> 
           <p> {{item.title}} </p>
        </div>
    </div>
    <TodoItem/>
</template>

<script>
import TodoItem from './TodoItem'

export default{
    name: 'Todos',
    props: ["todos"],
    components:{
        TodoItem
    }
}
</script>

<style scoped>
    #todo-holder{
        box-sizing: border-box;
        background-color: white;
        margin-top: 10px;
    }
    
    .todo-div{
        border: solid;
        margin-top: 10px;
        background-color: #DEB887;

    }
</style>