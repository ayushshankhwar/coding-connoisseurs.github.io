<template>
  <div>
    <div v-for="ele in data" :key="ele.name" class="card text-white bg-dark mb-3">
      <div class="card-body">
        <h5 class="card-title">{{ ele.title }}</h5>
        <p class="card-text">
          {{ ele.description }}
        </p>
        <a :href="`${ele.link}`">
          <button type="button" class="btn btn-light">Get Started</button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import pm from '../data/pm.json';
export default {
  name: 'PMResources',
  data() {
    return {
      data: pm,
    };
  },
};
</script>

<style scoped></style>
