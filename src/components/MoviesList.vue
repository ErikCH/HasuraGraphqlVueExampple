<template>
  <div class="list-of-movies">
    <movie-item v-for="movie in movies" :key="movie.id" :movie="movie" class="movie-item"></movie-item>
  </div>
</template>

<script>
import MovieItem from "./MovieItem";
import gql from "graphql-tag";
const GET_MOVIES = gql`
  query getMovies {
    movies {
      id
      title
      director
      composer
      release_date
    }
  }
`;
export default {
  name: "MoviesList",
  components: { MovieItem },
  data() {
    return {
      movies: []
    };
  },
  apollo: {
    movies: {
      query: GET_MOVIES
    }
  }
};
</script>

<style>
.list-of-movies {
  display: flex;
  justify-content: center;
}
.movie-item {
  margin: 0 10px;
}
</style>
