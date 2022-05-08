<template>
  <input type="text" placeholder="your name" v-model="enteredUsername" />
  <input type="number" placeholder="your age" v-model="enteredUserage" />
  <button @click="submitInput">Set User Data</button>
</template>

<script>
export default {
  emits: ["add-input-values"],
  data() {
    return {
      enteredUsername: "",
      enteredUserage: "",
    };
  },
  methods: {
    submitInput() {
      this.$emit("add-input-values", this.enteredUsername, this.enteredUserage);
    },
  },
};
</script>
