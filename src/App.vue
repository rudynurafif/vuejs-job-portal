<script>
export default {
  data() {
    return {
      name: 'John Doe',
      status: 'pending',
      tasks: ['Task One', 'Task Two', 'Task Three'],
    };
  },
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
</template>
