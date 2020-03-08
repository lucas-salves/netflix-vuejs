<template>
    <h1> {{titulo}} </h1>
</template>

<script>
  export default{
    name: 'teste',
    props: ['titulo']
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
  color: red;
}
</style>