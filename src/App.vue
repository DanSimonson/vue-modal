<template>
  <div id="app">
    <button type="button" class="btn" @click="showModal">Open Modal!</button>
    <modal
    v-show="isModalVisible"
    @close="closeModal"
  />
</div>
    <!--
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    -->
  </div>
</template>

<script>
  import Modal from "./components/Modal.vue";

  export default {
    name: "app",
    components: {
      Modal
    },
    data() {
      return {
        isModalVisible: false
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    }
  };
</script>

<style>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
