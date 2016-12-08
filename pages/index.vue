<template>
  <section class="container">
    <img src="~static/logo.png" alt="Nuxt.js Logo" />
    <ul>
      <li v-for="person in people">{{person.name}}</li>
    </ul>
  </section>
</template>

<style scoped>
.title
{
  margin: 50px 0;
}
</style>

<script>

import axios from 'axios'
const api = `https://swapi-json-server-nvaxelgbew.now.sh/people`

  export default {
    data(){
      return axios.get(api).then((res) => ({
        people: res.data
      }))
    }
  }
</script>
