<template>
  <div id="app" class="container">
    <Header/>
    <Todo/>
  </div>
</template>

<script>
import Todo from "./components/Todo.vue";

export default {
  name: "app",
  components: {
    Todo
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
.container {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: row wrap;
}
</style>
