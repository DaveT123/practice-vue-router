<template>
  <div>
    <h1>List of jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: { id: job.id }}">
         <h2>{{ job.title }}</h2>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jobs',
  data() {
    return {
      jobs: [
        { title: 'Dev 1', id: 1, details: 'John' },
        { title: 'Dev 2', id: 2, details: 'Peter' },
        { title: 'Dev 3', id: 3, details: 'Loon' }
      ]
    }
  }
}
</script>

<style>
    .job h2{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
  }
  .job h2:hover {
    background: #ddd;
  }
  .job a{
    text-decoration: none;
  }
</style>