<script setup>
defineProps({
    title: String
})
</script>

<template>
  <div class="banner">
    <div class="banner-text">
      <h1 class="banner-title">Carbon Credits su Blockchain</h1>
      <p class="banner-subtitle">Crediti di carbonio certificati su Blockchain</p>
    </div>
    <img class="banner-img" :src=this.title>
  </div>
</template>

<style scoped>
  .banner {
    background: #222638;
    height: 200px;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .banner-text {
    padding-left: 80px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    color: #FFFFFF;
  }

  .banner-title {
    font-size: 40px;
  }

  .banner-subtitle {
    font-size: 20px;
  }
  .banner-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    overflow: hidden;
  }
</style>
