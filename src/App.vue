<template>
  <div id="app">
    <button class="button">bulma</button>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'App',
  data(){
    return{
      pokemons: []
    }
  },
  components: {

  },
  methods:{

  },
  props:{

  },
  created: function(){
    console.log("INICIANDO APP");
    console.log("INICIANDO AXIOS" + axios);
    axios.get("https://pokeapi.co/api/v2/pokemon?limit=151&offset=0").then((res) => {
      this.pokemons = res.data.results;
      console.log(this.pokemons);
    });
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
  margin-top: 60px;
}
</style>
