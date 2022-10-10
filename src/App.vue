<template>
  <div id="app">
    <main>
      <div class="navigation">
        <header>
          <h1>Jakhongir Kholikulov</h1>
        </header>
        <nav>
          <a href="#">About Us</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <Progressbar :progress="progress"/>
      <Post @progressUpdate="setProgress" />
    </main>

  </div>
</template>

<script>
import Post from '@/components/Post';
import Progressbar from '@/components/Progressbar'
export default {
  name: 'App',

  components:{
    Post,
    Progressbar,
  },
  data(){
    return{
      progress: 0
    }
  },
  methods:{
    setProgress(progress){
      this.progress = progress
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
  font-family: 'monospace', sans-serif;
}

main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  overflow: hidden;
}

.navigation {
  width: 100%;
  height: 10vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #002337;
  padding: 30px;
}
header h1{
  color: #fff;
  font-size: 32px;
  /* text-align: center; */
}
nav a{
  margin: 0 20px;
  text-transform: uppercase;
  text-decoration: none;
  color: #fff;
}
</style>