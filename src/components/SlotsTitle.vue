<script>
export default {};
</script>

<template>
  <h1>
    <img src="../assets/logo.png" alt="" />
    <slot></slot>
  </h1>
</template>

<style scoped>
h1 {
  color: #fff;
  font-size: 50px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin-bottom: 30px;
}
img {
  display: block;
  width: 25px;
  margin-right: 10px;
}
</style>
