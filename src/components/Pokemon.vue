<template>
  <div id="pokemon">
      <h2>{{num}} - {{nome}}</h2>
      <small>{{url}}</small>
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    props:{
        num: Number,
        nome: String,
        url: String
    }

}
</script>

<style>

</style>