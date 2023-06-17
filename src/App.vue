<script setup>
  import Card from './components/Card.vue'
  import submissions from "./data/submissions.json"
</script>

<template>
  <main>
    <h1>Josh's Frontend Mentor Submissions</h1>
    <div class="grid">
      <Card v-for="submission in submissions" :key="submission.id" :img="submission.img" :heading="submission.heading" :languages="submission.languages" :description="submission.description" :link="submission.link" />
  </div>
  </main>
  

  
</template>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,400;0,500;0,600;0,700;1,500;1,600&display=swap');


main {
  margin: 0 auto;
  margin-top: 2rem;
  max-width: 95rem;
  justify-content: center;
}

h1 {
  text-align: center;
  font-family: 'Barlow', sans-serif;
  font-weight: 300;
}

.filters {
  text-align: center;
}


.grid {
  display: grid;
  place-items: center;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  grid-column-gap: 0.5rem;
  grid-row-gap: 2rem;
  align-items: center;
}

</style>


