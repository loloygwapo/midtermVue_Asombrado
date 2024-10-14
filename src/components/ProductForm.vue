<template>
  <div>
    <form @submit.prevent="addTask">
      <input type="text" v-model="newTask" placeholder="Enter product name" />
      <input type="price" v-model="task" placeholder="Enter a price" />
      <input type="description" v-model="task1" placeholder="Enter description" />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTask: "",
    };
  },
   data() {
    return {
      task: "",
    };
  },
   data() {
    return {
      task1: "",
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim()) {
        this.$emit("add-task", this.newTask);
        this.newTask = "";
      }
    },
  },
  methods: {
    addTask() {
      if (this.task.trim()) {
        this.$emit("add-task", this.task);
        this.task = "";
      }
    },
  },
  methods: {
    addTask() {
      if (this.task1.trim()) {
        this.$emit("add-task", this.task1);
        this.task1 = "";
      }
    },
  },
};


</script>

