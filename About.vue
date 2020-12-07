<template>
  <div>
    <h3>About</h3>
    <div v-if="showMsg">
      <input type="text" v-model="title" />
      <button @click="showMessage">Hide message</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      title: "",
      showMsg: true
    };
  },

  methods: {
    showMessage() {
      this.showMsg = false;
    }
  },

  beforeCreate() {
    console.log("beforecreate");
  },

  created() {
    console.log("created");
  },

  beforeMount() {
    console.log("beforeMount");
  },

  mounted() {
    console.log("mounted");
  },

  beforeUpdate() {
    console.log("beforeUpdate");
  },

  updated() {
    console.log("updated");
  },

  beforeDestroy() {
    console.log("beforeDestroy");
  },

  destroyed() {
    console.log("destroyed");
  }
};
</script>

<style scoped>
.navbar {
  background: #1a1d24;
}

.navbar-nav a {
  color: #fff;
  padding: 0 15px;
  display: block;
}

h3 {
  color:white;
}
</style>