<template>
  <header>
    <h1>{{ title }}</h1>
    <ButtonVue
      v-show="homePage"
      @button-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import ButtonVue from "./Button.vue";

export default {
  name: "Header",
  // props: ['title']
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    ButtonVue,
  },
  computed: {
    homePage() {
      return this.$route.path == "/";
    },
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>