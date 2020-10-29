<template>
  <button v-if="showClearCompletedButton" @click="clearCompleted">
    Clear Completed
  </button>
</template>

<script>
import { mapGetters } from 'vuex';
export default {
  name: 'todo-clear-completed',

  computed: {
    ...mapGetters(['showClearCompletedButton']),
  },

  methods: {
    clearCompleted() {
      this.$store.dispatch('clearCompleted');
    },
  },
};
</script>