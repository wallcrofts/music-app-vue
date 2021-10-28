<template>
  <div id="app">
    <header>
      <h1>My music</h1>
    </header>
    <main>
      <section class="player">
          <h2 class="song-title">{{ current.title }} <span>- {{ current.artist }}</span> </h2>
      </section>
    </main>
  </div>
</template>

<script>

  export default {
    name: 'App',
    data () {
      return {
        current: {},
        index: 0,
        songs: [
          {
            title: 'Alive',
            artist: 'Sam Hulick',
            src: require('./assets/alive.mp3')
          },
          {
            title: 'Citadel',
            artist: 'Jack Wall...',
            src: require('./assets/citadel.mp3')
          },
          {
            title: 'Gear Up',
            artist: 'Sam Hulick',
            src: require('./assets/gearup.mp3')
          },
        ],
        player: new Audio()
      }
    },
    created () {
      this.current = this.songs[this.index];
      this.player.src = this.current.src;
      this.player.play();
    }
  }

</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;

  }
  body {
    font-family: sans-serif;
  }
  header {
    display: flex;
    align-content: center;
    justify-content: center;
    padding: 15px;
    background-color: #161616;
    color: white;
  }
</style>