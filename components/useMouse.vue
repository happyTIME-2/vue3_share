<template>
  <div
    grid="~ flow-col gap-4"
    place="content-center items-center"
    h="screen"
    font="mono"
    >
    <Coordinate label="X" :value="x" />
    <Coordinate label="Y" :value="y" />
  </div>
</template>
<script lang="ts" setup>
import { useMouse } from '@vueuse/core'
import Coordinate from './Coordinate.vue'

const { x, y } = useMouse()
</script>
<style scoped>
div{height: 100px}
</style>