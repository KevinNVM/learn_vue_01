<template>
  <button
    @click="$emit('button-click')"
    :style="{ backgroundColor: color }"
    class="btn"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods: {},
};
</script>