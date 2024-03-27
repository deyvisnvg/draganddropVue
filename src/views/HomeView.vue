<script>
import SongPlayer from '@/components/SongPlayer.vue'

export default {
  name: 'HomeView',
  components: {
    SongPlayer
  },
  data() {
    return {
      songData: null
    }
  },
  methods: {
    songs() {
      const songs = [
        {
          "id": 1,
          "name": "A puro dolor",
          "artist": "Sin bandera",
          "album": "Album 1",
          "year": 2015,
          "genero": "Baladas",
          "duration": 120,
          "estado": "privado",
        },
        {
          "id": 2,
          "name": "Ya me enteré",
          "artist": "Reik",
          "album": "Album 1",
          "year": 2016,
          "genero": "Baladas",
          "duration": 120,
          "estado": "privado",
        },
        {
          "id": 3,
          "name": "Noviembre sin tí",
          "artist": "Reik",
          "album": "Album 1",
          "year": 2005,
          "genero": "Baladas",
          "duration": 120,
          "estado": "privado",
        }
      ]

      this.songData = songs
    }
  },
  created() {
    this.songs();
  }
}

</script>

<template>
  <div>
    <h1 class="text-center font-bold text-2xl">Lista de canciones</h1>
    <SongPlayer :dataSong="songData"/>
  </div>
</template>
