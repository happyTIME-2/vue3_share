<template>
<div class="rounded bg-green-500/50 p-2 mt-1">
  <p>FullName: {{fullName}}</p>
  <p class="rounded-2xl mt-2"><button @click="show">Click</button></p>
</div>
</template>
<script lang="ts">
import { defineComponent, toRefs, computed } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    name: {
      type: String,
      default: ''
    },
    job: {
      type: String,
      default: 'Development Engineer'
    }
  },
  setup(prop: any) {
    const { name, job } = toRefs(prop);

    const fullName = computed(() => `${name.value}`);

    const show = () => {
      alert(job.value)
    }

    return {
      fullName,
      show
    }
  },
})
</script>
