<template>
  <h1>User: {{ id }}</h1>
</template>

<script>
export default {
  computed: {
    id() {
      return this.$route.params.id;
    }
  },
  validate({ params }) {
    // Must be a number
    return /^\d+$/.test(params.id);
  },
};
</script>
