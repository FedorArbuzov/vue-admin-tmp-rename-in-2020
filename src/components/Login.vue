<template>
  <div>
    <p>login</p>
    <p>{{ count }}</p>
  </div>
</template>

<script>
export default {
  name: "Login",
  computed: {
    count() {
      return this.$store.state.count;
    }
  }
};
</script>
