<template>
    <ul>
      <li v-for="country in countries" :key="country.id">{{ country.name }}</li>
    </ul>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { supabase } from './lib/supabaseClient'

const countries = ref([])

async function getCountries() {
  const { data } = await supabase.from('countries').select()
  countries.value = data
}

onMounted(() => {
  getCountries()
})
</script>


<template>
  <h1>Food</h1>
  <personal-profile/><br>
  <food-item/><br>
  <food-item2/><br>
  <food-item/><br>
  <food-item2/><br>
</template>

<script></script>

<style></style>