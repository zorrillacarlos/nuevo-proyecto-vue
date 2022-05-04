<template>
  <div class="container mb-5">
    <h1 class="text-center mb-5">CHARACTERS RICK AND MORTY</h1>
    <div class="row justify-content-center">
      <div v-for="(item, index) in result" :key="index" class="card col-6 col-sm-2 m-3 p-0">
        <img v-bind:src="item.image" class="card-img-top" v-bind:alt="item.name"/>
        <div class="card-body">
          <h5 class="card-title">{{ item.name }}</h5>
          <p class="card-text">Origen: {{ item.origin.name }}</p>
          <p class="card-text">Estado: {{ item.status }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// https://codingpotions.com/vue-axios
// https://es.vuejs.org/v2/guide/list.html
// https://www.youtube.com/watch?v=B8rVlxQm8Cs
// https://youtu.be/7iDGJolHFmU

//import axios from "axios";

export default {
/*   data: () => ({
    result: null,
  }),
  created() {
   axios.get("https://rickandmortyapi.com/api/character").then((result) => {
      this.result = result.data.results;
    });
  }, */

  data(){
    return {
      result: null
      }
  },
  mounted(){
      fetch("https://rickandmortyapi.com/api/character")
      .then(res => res.json())
      .then(data => this.result = data.results)
  }
};

</script>

<style></style>
