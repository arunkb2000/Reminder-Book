<template>
    <header>
        <h1> {{title}}</h1>
        <Button  @btn-click ="$emit('toggle-add-task')" 
        :text ="showAddTask ? 'Close' : 'Add'"
        :color ="showAddTask ? 'red' : 'green'"/>
       
        
    </header>
</template>

<script>
import Button from './Button'

export default {
    name: 'Header',
    //props: ['title'],
    //another way we can do this 
    props: {
      title: String,
    showAddTask: Boolean,
    },
   //  default: " This is a earlier message."  
   // default message will display when there where nothing is defined in App.vue files component Header.
   // }
   components: {
       Button,
   },
}
</script>
<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>