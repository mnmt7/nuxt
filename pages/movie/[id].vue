<template>
  <div class="container">
    <h1 class="movie-title">{{ movie.title }}</h1>
    <img :src="movie.image" :alt="movie.title" class="movie-image">
    <p class="movie-description">{{ movie.description }}</p>
  </div>
</template>

<script setup>
const route = useRoute();
const movies = [
  { id: 1, title: 'The Shawshank Redemption', description: 'Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.', image: 'https://m.media-amazon.com/images/I/51R0XUE2OAL.jpg' },
  { id: 2, title: 'The Godfather', description: 'The aging patriarch of an organized crime dynasty transfers control of his clandestine empire to his reluctant son.', image: 'https://via.placeholder.com/300x450?text=The+Godfather' },
  { id: 3, title: 'The Dark Knight', description: 'When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, Batman must accept one of the greatest psychological and physical tests of his ability to fight injustice.', image: 'https://via.placeholder.com/300x450?text=The+Dark+Knight' },
  { id: 4, title: 'Pulp Fiction', description: 'The lives of two mob hitmen, a boxer, a gangster and his wife, and a pair of diner bandits intertwine in four tales of violence and redemption.', image: 'https://via.placeholder.com/300x450?text=Pulp+Fiction' },
  { id: 5, title: 'Forrest Gump', description: 'The presidencies of Kennedy and Johnson, the Vietnam War, the Watergate scandal and other historical events unfold from the perspective of an Alabama man with an IQ of 75, whose only desire is to be reunited with his childhood sweetheart.', image: 'https://via.placeholder.com/300x450?text=Forrest+Gump' },
  { id: 6, title: 'Inception', description: 'A thief who steals corporate secrets through the use of dream-sharing technology is given the inverse task of planting an idea into the mind of a C.E.O.', image: 'https://via.placeholder.com/300x450?text=Inception' },
];

const movie = movies.find(movie => movie.id === +route.params.id)
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.movie-title {
  font-size: 2.5em;
  margin-bottom: 20px;
  color: #e50914;
}

.movie-image {
  width: 100%;
  max-width: 300px;
  height: auto;
  border-radius: 4px;
  margin-bottom: 20px;
}

.movie-description {
  font-size: 1.1em;
  line-height: 1.6;
  margin-bottom: 20px;
}

.back-link {
  display: inline-block;
  padding: 10px 20px;
  background-color: #e50914;
  color: #ffffff;
  text-decoration: none;
  border-radius: 4px;
  transition: background-color 0.3s ease;
}

.back-link:hover {
  background-color: #f40612;
}
</style>