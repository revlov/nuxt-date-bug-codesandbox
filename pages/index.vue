<template>
  <div class="container">
    <h1>My simplified Schedule</h1>
    <MySchedule />
  </div>
</template>

<script>
  import MySchedule from '~/components/MySchedule'

  export default {
    components: {
      MySchedule
    }
  }
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
</style>
