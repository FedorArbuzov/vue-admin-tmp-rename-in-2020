<template>
  <div>
    <h1>Hello</h1>
    <p>{{ count }}</p>
    <button v-on:click="inc">hello</button>
    <button v-on:click="go">login</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  beforeCreate: function() {
    console.log("before created"); // eslint-disable-line no-console
  },
  computed: {
    count() {
      return this.$store.state.count;
    }
  },
  methods: {
    inc: function() {
      return this.$store.commit("increment");
    },
    go: function() {
      this.$router.push({ name: "Login" });
    }
  }
};
</script>
