<template>
  <div class="container">
    <h1 class="title">Movie List</h1>
    <div class="movie-grid">
      <div v-for="movie in movies" class="movie-card">
        <a :href="`/movie/${movie.id}`">
          <img :src="movie.image" :alt="movie.title" class="movie-image">
          <div class="movie-title">{{ movie.title }}</div>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
const movies = [
  { id: 1, title: 'The Shawshank Redemption', description: 'Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.', image: 'https://m.media-amazon.com/images/I/51R0XUE2OAL.jpg' },
  { id: 2, title: 'The Godfather', description: 'The aging patriarch of an organized crime dynasty transfers control of his clandestine empire to his reluctant son.', image: 'https://m.media-amazon.com/images/I/71khjV-MoOS._AC_UF894,1000_QL80_.jpg' },
  { id: 3, title: 'The Dark Knight', description: 'When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, Batman must accept one of the greatest psychological and physical tests of his ability to fight injustice.', image: 'https://m.media-amazon.com/images/I/81CLFQwU-WL._AC_UF1000,1000_QL80_.jpg' },
  { id: 4, title: 'Pulp Fiction', description: 'The lives of two mob hitmen, a boxer, a gangster and his wife, and a pair of diner bandits intertwine in four tales of violence and redemption.', image: 'https://via.placeholder.com/300x450?text=Pulp+Fiction' },
  { id: 5, title: 'Forrest Gump', description: 'The presidencies of Kennedy and Johnson, the Vietnam War, the Watergate scandal and other historical events unfold from the perspective of an Alabama man with an IQ of 75, whose only desire is to be reunited with his childhood sweetheart.', image: 'https://m.media-amazon.com/images/I/713xd8jGVuL._AC_UF1000,1000_QL80_.jpg' },
  { id: 6, title: 'Inception', description: 'A thief who steals corporate secrets through the use of dream-sharing technology is given the inverse task of planting an idea into the mind of a C.E.O.', image: 'https://via.placeholder.com/300x450?text=Inception' },
];
</script>

<style scoped>
.container {
  max-width: 700px;
  margin: 0 auto;
  padding: 20px;
}

.title {
  font-size: 2.5em;
  margin-bottom: 20px;
  color: #e50914;
}

.movie-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 20px;
}

.movie-image {
  width: 100%;
  height: auto;
  border-radius: 4px;
}

.movie-title {
  margin-top: 10px;
  font-size: 1em;
  text-align: center;
}

a {
  text-decoration: none;
  color: #ffffff;
}
</style>