<script setup>
defineProps({
  key: Number,
  img: String,
  heading: String,
  languages: Object,
  description: String,
  link: String
})


</script>



<template>
  <main class="card">
    <div class="card-image-container">
      <img class="card-image" :src="img" alt="">
    </div>
    <div class="card-content-container">
      <h1 class="card-heading">{{ heading }}</h1>
      <div class="card-languages-container">
        <h2 v-if="languages.HTML" class="language-html">HTML</h2>
        <h2 v-if="languages.CSS" class="language-css">CSS</h2>
        <h2 v-if="languages.JS" class="language-js">JS</h2>
        <h2 v-if="languages.API" class="language-api">API</h2>
      </div>
      <p class="card-description">{{ description }}</p>
      <div class="card-buttons-container">
        <a target=”_blank” class="card-button" :href="link">View Live Project</a>
      </div>      
    </div>
  </main>
</template>



<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,400;0,500;0,600;0,700;1,500;1,600&display=swap');
  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: fit-content;
    background-color: rgb(255, 255, 255);
    border-radius: 1rem;
    box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);

  }

  .card-image-container {
    display: flex;
    width: fit-content;
    border-radius: 1rem;

  }

  .card-image {
    max-width: 350px;
    border-radius: 1rem;
    border-bottom-left-radius: 0%;
    border-bottom-right-radius: 0%;
  }

  .card-content-container {
    display: flex;
    flex-direction: column;
    margin: 0;
    margin-top: 1.5rem;
    justify-content: center;
    width: 350px;
  }

  .card-heading {
    margin: 0;
    font-family: 'Barlow', sans-serif;
    font-weight: 500;
    font-size: 24px;
    margin-left: 1rem;
    margin-right: 1rem;
  }

  .card-languages-container {
    display: flex;
    flex-direction: row;
    margin-top: 1rem;
    margin-left: 1rem;
  }

  h2 { 
    font-family: 'Barlow', sans-serif;
    font-size: 20px;
    margin: 0;
    margin-right: 0.6rem;
  }

  .language-html {
    color: rgb(106, 190, 205);
  }

  .language-css {
    color: rgb(62, 84, 163);
  }

  .language-js {
    color: rgb(207, 99, 144);
  }

  .language-api {
    color: rgb(170, 215, 66);
  }

  .card-description {
    margin: 0;
    margin-top: 1rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 400;
    font-size: 16px;
    margin-left: 1rem;
    margin-right: 1rem;
    color: rgb(77, 77, 77)
  }

  .card-buttons-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-top: 2rem;
  }

  .card-button {
    background-color: rgb(82, 77, 219);
    padding: 0.6rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-decoration: none;
    color: white;
    border-radius: 0.5rem;
    flex: auto;
    text-align: center;
    font-weight: 500;
    border-top-left-radius: 0%;
    border-top-right-radius: 0%;
  }

  .card-button:hover {
    text-decoration: underline;
    cursor: pointer;
  }




</style>
