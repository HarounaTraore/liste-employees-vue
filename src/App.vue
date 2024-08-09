<template>
  <div class="contener">
    <h2>Liste des employées</h2>
  <ol>
    <li v-for="employee in employees" :key="employee">
      {{ employee }}
    </li>
  </ol>
  </div>
</template>

<script setup>
  import {ref} from 'vue';

  const employees = ref([
    'Assa Baradji',
    'Ousmane Ly', 
    'Thillo Seme',
    'Mamoudou Ba', 
    'Fatima Cissé',
    'Abdrahmane Thimbo',
    'Fatimata Sall',
    'Zouber Ba',
    'Mohamed Bankolé'
  ])
  
</script>
<style >
  body{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 90vh;
  }
  .contener{
    padding: 20px;
    border: 3px solid rgba(0, 0, 255, 0.304);
    border-radius: 5px;
    color: white;
    background-color: rgb(7, 160, 255);
    font-size: 18px;
    width: 500px;
  }
   li {
    border-bottom: 1px rgb(118, 242, 73) solid;
    padding: 5px;
   }
   ol li:hover {
    background-color: blue;
    transition-duration: 0.75s;
   }
   h2 {
    text-align: center;
   }
</style>