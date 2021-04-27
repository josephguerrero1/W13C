<template>
  <div>
    <h3>PlayList</h3>
    <div id="play-container">
      <div v-for="song in songs" :key="song.artist" class="song">
        <h4>{{ song.artist }}</h4>
        <h5>{{ song.song }}</h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    songs: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
#play-container {
  width: 40vw;
  margin-left: 5vw;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}

.song {
  box-shadow: 3px 3px 6px grey;
  min-width: 100px;
  min-height: 100px;
}
</style>
