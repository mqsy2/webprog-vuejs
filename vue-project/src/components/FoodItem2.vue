<template>
  <div class ="mango">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Mangoes',
      message: 'I like mangoes'
    }
  }
};
</script>

<style>
  .mango {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(250, 252, 162);
  }
</style>