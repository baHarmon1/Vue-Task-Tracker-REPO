<template>
<div :class="[task.reminder ? 'reminder' : '', 'task']" > <!--the class is task, but also, if the task.reminder is true, the class is also "reminder"-->
    <h3>{{task.text}}
    <i class="fas fa-times"></i></h3>
    <p>{{task.day}}</p>
</div>
</template>

<script>
    export default {
        name: "Task",
        props: {
            task: Object
        }
    }
</script>

<style>
.fas {
    color: black;
}
.fas:hover {
    color: red;
}
.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 10px 20px;
    cursor: pointer;
}
.task.reminder {
    border-left: 5px solid green;
}
.task h3{
    display:flex;
    align-items: center;
    justify-content: space-between;
}
</style>