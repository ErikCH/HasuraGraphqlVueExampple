<template>
  <div id="app">
    <div class="img-wrapper">
      <img alt="Vue logo" src="./assets/logo.png">
    </div>
    <add-movie/>
    <movies-list/>
  </div>
</template>

<script>
import MoviesList from "./components/MoviesList.vue";
import AddMovie from "./components/AddMovie.vue";

export default {
  name: "app",
  components: {
    MoviesList,
    AddMovie
  }
};
</script>
<style>
.app {
  margin: auto;
  width: 50%;
}
.img-wrapper {
  display: flex;
  justify-content: center;
}
</style>
