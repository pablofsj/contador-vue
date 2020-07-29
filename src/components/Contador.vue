<template>
  <div class="container">
    <div class="row">
      <div class="col-sm-12">
        <h1>Juego del Contador</h1>
        <br>
        <h5>Al clickear el boton aumentan los clicks totales y al hacer mouseover sobre el boton, el contador se reinicia a 0</h5>
        <br>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-12">
        <button  @click="sumarClicks()" @mouseenter="reiniciarClicks()" type="button" class="btn btn-outline-info">¡Clickeame!</button>
        <br><br>
      </div>
      <div class="col-sm-12">
        <h2>Clicks Totales: <span>{{count}}</span></h2>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name:'Contador',
  computed: {
    count() {
      return this.$store.state.count
    }
  },

  methods: {
    sumarClicks: function(){
      this.$store.commit('increment')

    },

    reiniciarClicks: function(){
      this.$store.commit('decrement')

    }

  }

};


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1{
  color: rgb(34, 191, 212);
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
