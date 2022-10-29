<template>
  <div id="app">
    <main>
      <div class="navigation">
        <header>
          <h1>Jamshidbek Razzaqov</h1>
        </header>
        <nav>
          <a href="#">About us</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <progressbar :progress="progress"/>
      <post @progressUpdate="setProgress"/>
    </main>
  </div>
</template>

<script>
import Post from './components/Post.vue'
import Progressbar from './components/Progressbar.vue'
export default {
  components: { Post, Progressbar },
  data() {
    return {
      progress: 0
    }
  },  
  methods: {
    setProgress(progress){
      this.progress = progress;
    }
  },
}
</script>
<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body{
    font-family: sans-serif;
  }
  main{
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    overflow: hidden;
  }
  .navigation{
    width: 100%;
    height: 10vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #002337;
    padding: 30px;
  }
  header h1{
    margin-left: 10px;
    font-size: 32px;
    color: aliceblue;
  }
  nav a{
    margin: 0 20px;
    text-decoration: none;
    color: #fff;
    text-transform: uppercase;
  }
</style>