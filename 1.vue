<template>
  <div class="child-two">
    <div class="dv" :style="{ backgroundColor: bgColorStyle, border: borderStyle }" id="dv">测试
    </div>
    <div class="dv" :style="styleObj">
    </div>

  </div>
</template>

<script setup lang="ts">
import { ref} from 'vue'

const bgColorStyle = ref()


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
  margin-left: 22px;
  .dv {
    width: 100px;
    height: 100px;
    margin-bottom: 10px;
    .css{
     font-size:12px;
    }
  }
}
</style>