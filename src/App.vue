<script>
export default {
  data() {
    return {
      name: 'John Doe',
      status: 'pending',
      tasks: ['Task One', 'Task Two', 'Task Three'],
      link: 'https://google.com'
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') this.status = 'pending'
      else if (this.status === 'pending') this.status = 'inactive'
      else this.status = 'active'
    }
  }
};
</script>

<template>
  <h1>{{ name }}</h1>

  <br>

  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <br>

  <h3>Task:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <!-- <a v-bind:href="link">Go to Google</a> -->
  <a :href="link">Go to Google</a>

  <br>

  <!-- <button v-on:click="toggleStatus">Change Status</button> -->
  <button @click="toggleStatus">Change Status</button>
</template>
