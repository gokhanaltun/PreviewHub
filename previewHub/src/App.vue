<script setup>
import { projects } from '@/data/db';
import ProjectCard from '@/components/ProjectCard.vue'
import { onMounted, reactive } from 'vue';

const state = reactive({
  projectArray: []
})

onMounted(() => {
  state.projectArray = projects
})
</script>

<template>
  <div class="container mt-5">
    <h1 class="text-center mb-4">Vue.js Projects</h1>
    <div class="row">
      <ProjectCard v-for="project in state.projectArray" :key="project.id" :project="project"/>
    </div>
  </div>
</template>
