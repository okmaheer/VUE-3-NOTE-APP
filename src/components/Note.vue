<template>
    
    <div  class="card mb-4" >
      <div class="card-content">
        
        <div class="content">
        {{ note.content }}
        <small>{{ characterLength }}</small>
        </div>
      </div>
      <footer class="card-footer">
        <a href="#" class="card-footer-item">Edit</a>
        <a href="#" class="card-footer-item">Delete</a>
      </footer>
    </div>
</template>
<script setup>
import {computed} from 'vue'
const props = defineProps({
    note:{
        type: Object,
        required:true,
    }
})
const characterLength = computed(() =>{
 return props.note.content.length;
})
</script>