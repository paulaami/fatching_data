<template>
  <user-data @add-input-values="setUserData"></user-data>
  <active-user :username="user.name" :userage="user.age"></active-user>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "Paula",
        age: 31,
      },
    };
  },
  methods: {
    setUserData(name, age) {
      this.user = {
        name: name,
        age: +age,
      };
    },
  },
};
</script>
