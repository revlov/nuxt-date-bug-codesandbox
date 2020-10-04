<template>
  <div class="schedule">
    <div
      v-for="s in schedule"
      :key="s.id"
      :class="{ 'current': getCurrentDay() === s.id }"
      class="day"
    >
      {{ s.day }}
    </div>
  </div>
</template>

<script>
  export default {

    name: 'MySchedule',

    props: {
      schedule: {
        type: Array,
        default: () => [
          { id: 0, day: 'Sun', items: [] },
          { id: 1, day: 'Mon', items: [] },
          { id: 2, day: 'Tue', items: [] },
          { id: 3, day: 'Wed', items: [] },
          { id: 4, day: 'Thu', items: [] },
          { id: 5, day: 'Fri', items: [] },
          { id: 6, day: 'Sat', items: [] },
        ],
      }
    },

    methods: {
      getCurrentDay() {
        return new Date().getDay()
      }
    },
  }
</script>

<style lang="scss">
  .schedule {
    display:    flex;
    margin-top: 1rem;
  }

  .day {
    display:         flex;
    align-items:     center;
    justify-content: center;
    width:           2.5rem;
    height:          2.5rem;
    margin:          0 0.125rem;
    cursor:          pointer;
    user-select:     none;
    border:          0.1rem solid black;

    &:hover {
      background: grey;
    }

    &.current {
      background: orange;

      &:hover {
        background: coral;
      }
    }
  }
</style>
