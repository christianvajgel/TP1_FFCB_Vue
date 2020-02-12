<template>
  <ul>
    <li v-for="(value) in tasks" :key="value">
      <p v-if="value.isCompleted === true" class="greenText">ID: {{ value.id }} | Description: {{ value.description }} | Completed </p>
      <p v-else class="redText">ID: {{ value.id }} | Description: {{ value.description }} |  On Progress </p>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Tasks',
  data:function() {
    return {
      tasks : [
        {
          id: 1,
          description:'Description of task #1',
          isCompleted: true
        },
        {
          id: 2,
          description:'Description of task #2',
          isCompleted: false
        },
        {
          id: 3,
          description:'Description of task #3',
          isCompleted: false
        } ,
        {
          id: 4,
          description:'Description of task #4',
          isCompleted: true
        }
      ]
    };
  }
}
</script>

<style scoped>
  ul {
    list-style-type: none;
  }

  .redText {
    color: red !important;
  }

  .greenText {
    color: green !important;
  }
</style>