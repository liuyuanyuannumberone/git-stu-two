<template>
  <div class="child-two">
    <div class="dv" :style="{ backgroundColor: bgColorStyle, border: borderStyle }"></div>
    <div class="dv" :style="styleObj"></div>
    <div class="dv" :style="[styleObj]"></div>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const bgColorStyle = ref()
const borderStyle = ref()

const styleObj = computed(() => ({
  backgroundColor: bgColorStyle.value,
  border: borderStyle.value
}))
</script>

<script lang="ts">
export default {
  name: 'BindStyle'
}
</script>

<style lang="less" scoped>
.child-two {
  margin-left: 20px;
  .dv {
    width: 100px;
    height: 100px;
    background-color: #eee;
    margin-bottom: 10px;
  }
}
</style>