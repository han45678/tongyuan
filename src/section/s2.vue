<script setup>
import Fullview from '../components/fullview.vue';
</script>

<template>
  <article class="s2 relative" id="s2">

    <div class="map hidden md:block">
      <img src="@/section/s2/map.webp" alt="bg_decor">
    </div>

    <div class="map block md:hidden">
      <Fullview />
    </div>

  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s2 {
  // background: #C7000B;
  width: 100%;
  position: relative;
  padding: size(40);
  box-sizing: border-box;
  .map{
    position: relative;
    z-index: 1;
  }
}
</style>
