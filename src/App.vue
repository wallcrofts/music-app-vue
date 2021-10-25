<template>
  <div id="app">
    <header>
      <h1>My music</h1>
    </header>
    <main>
      <section class="player">
          <h2 class="song-title">{{ current.title }}</h2>
      </section>
    </main>
  </div>
</template>

<script>

  export default {
    name: 'App',
    data () {
      return {
        current: 'SONG TITLE'
      }
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