<template>
  <section class="container">
    <img src="~static/logo.png" alt="Nuxt.js Logo" />
    <h1 class="title">
      {{message}}
    </h1>
    <input v-model="message">
  </section>
</template>

<style scoped>
.title
{
  margin: 50px 0;
}
</style>

<script>
  export default {
    data(){
      return {
        message: "Hello World!"
      }
    }
  }
</script>
