<template>
  <div class="anime-card">
    <img :src="anime.images.jpg.image_url" alt="Anime Image" class="anime-image">
    <div class="anime-info">
      <h3>{{ anime.title }}</h3>
      <p>{{ anime.synopsis }}</p>
      <router-link :to="{ name: 'AnimeDetails', params: { id: anime.mal_id } }" class="details-link">View Details</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "AnimeCard",
  props: {
    anime: Object
  }
};
</script>

<style scoped>
.anime-card {
  border: 1px solid #ccc;
  border-radius: 10px;
  margin: 10px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f9f9f9;
}

.anime-image {
  max-width: 100%;
  border-radius: 10px;
}

.anime-info {
  text-align: center;
}

.details-link {
  color: #3498db;
  text-decoration: none;
  margin-top: 10px;
  display: inline-block;
}

.details-link:hover {
  text-decoration: underline;
}
</style>
