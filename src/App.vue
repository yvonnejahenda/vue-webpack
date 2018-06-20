<template>
  <div class="container">
    <h3>{{ title }}</h3>
    <form>
    <textarea placeholder = "Add new task" v-model="newTask"></textarea>
    <P>{{newTask}}</p>
    <button type="button" v-on:click="addTask">AddTask{{tasks.length}}</button>
    </form>
    <ul>
    <li v-for="task in tasks">{{task}}</li>
    </ul>

  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'My Todo List',
      newTask:'This is a sample',
     
     
      tasks:[]
    }
  },
  methods:{
  	addTask(){
  		
  		this.tasks.unshift(this.newTask);
  		this.newTask='';


  	}
  }

}
</script>
