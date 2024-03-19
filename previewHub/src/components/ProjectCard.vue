<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    project: {
        type: Object,
        require: true
    }
})

</script>

<template>
    <div class="col-lg-4 col-md-6 mb-4">
        <div class="card" style="box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
            <div class="card-body">
                <h5 class="card-title">{{ props.project.title }}</h5>
                <p class="card-text">{{ props.project.description }}</p>
                <a :href="props.project.previewUrl" class="btn btn-primary">preview</a>
            </div>
        </div>
    </div>
</template>