<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/data">data</router-link>
    <!-- <router-link to="/about">About</router-link> -->
  </nav>
  <router-view/>

  <Footer/>  <!---the footer-->
</template>

<script>
     import Footer from "@/components/Footer.vue";
  export default {
      components:{
        Footer
      }
    }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

nav {
  padding: 30px;
  background-color: #2c3e50;
}

nav a {
  font-weight: bold;
  color: white;
  text-decoration: none;
}
 
nav a.router-link-exact-active {
  color: white;
}

.card-body{
  background-color: #2c3e50;
  color: white;
  font-weight: bold;
  border: 1px solid white;
  text-align: center;
  padding: 30px;
  margin:4px 10%;
  border-radius:5px ;
}

#display{
  margin-bottom: 40%;
}
</style>
