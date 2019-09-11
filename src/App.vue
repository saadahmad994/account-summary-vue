<template>
  <div id="app">
    <test />
  </div>
</template>

<script>
import test from "./test";
export default {
  name: "app",
  components: {
    test: test
  },
  data() {
    return {
      title: "My First Vue.js App",
      friends: [
        { name: "Saad", online: true },
        { name: "Deepak", online: true },
        { name: "Puneet", online: false },
        { name: "Abhishek", online: false }
      ]
    };
  },
  methods: {
    deleteFriend(payload) {
      this.friends = this.friends.filter(friend => {
        return friend.name !== payload.name;
      });
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
