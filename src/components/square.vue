<template>
  <div v-html="text" class="square" v-bind:class="size" v-bind:style="{backgroundColor:color}">
  </div>
</template>

<script>
export default {
  name: 'Square',
  props: {
    color: String,
    size: String,
    text: String,
    title: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .square {
    background-color: rgb(255, 255, 255);
    color: rgb(255, 255, 255);
    margin: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
</style>