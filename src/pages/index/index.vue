<script setup lang="ts">
import { ref, onMounted } from 'vue';
import CategoryPanel from './components/categoryPanel.vue';
const noticeText = ref('这是一条滚动通知');

onMounted(() => {
  // 模拟滚动
  setInterval(() => {
    noticeText.value += ' ';
  }, 1000);
});
</script>

<template>
  <CztySwiper />
  <uni-notice-bar :show-icon="true" :scrollable="true" :text="noticeText" mode="closeable" :speed="50" />
  <categoryPanel />
  <CztyAutoVerticalNotice />
  <CztyVideoSwiper />
</template>

<style lang="scss">
page {
  background-color: #f7f7f7;
}
</style>
