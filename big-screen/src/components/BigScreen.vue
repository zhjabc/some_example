<script setup>
import autofit from 'autofit.js'
import {BorderBox1, BorderBox12, BorderBox13} from '@dataview/datav-vue3';
import {onMounted, onUnmounted} from "vue";

onMounted(() => {
  autofit.init({
    el: '#big-screen',
  })
})

onUnmounted(() => {
  autofit.off()
})

</script>

<template>
  <div id="big-screen" class="big-screen">
    <div class="big-screen-content">
      <h1 class="title">大屏展示</h1>
      <div class="main-content">
        <BorderBox1 class="container1"/>
        <BorderBox1 class="container1"/>
        <BorderBox1 class="container1"/>
        <BorderBox12 class="container1"/>
        <BorderBox12 class="container1"/>
        <BorderBox12 class="container1"/>
        <BorderBox13 class="container1"/>
        <BorderBox13 class="container1"/>
        <BorderBox13 class="container1"/>
      </div>
    </div>
  </div>
</template>

<style scoped>

.big-screen-content {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  padding: 30px;
  background: url("@/assets/bg.png") no-repeat;
  background-size: 100% 100%;
  box-sizing: border-box;
}

.title {
  text-align: center;
  color: #fff;
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 15px;
}

.main-content {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 三列 */
  grid-template-rows: repeat(3, 1fr); /* 三行 */
  gap: 10px 30px; /* 网格间隙 */
}

</style>