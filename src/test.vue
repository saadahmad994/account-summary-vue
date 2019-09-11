<template>
  <div id="all-friends">
    <h3>All Friends</h3>
    <div v-for="(friend, index) in friends" :key="index">
      <span @click="unfriend(friend.name)">{{friend.name}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "AllFriend",
  props: ["friends"],
  data() {
    return {};
  },
  methods: {
    unfriend(name) {
      this.$emit("delete", { name: name });
    }
  }
};
</script>

<style>
</style>