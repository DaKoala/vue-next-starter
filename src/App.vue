<template>
  <img src="./logo.png">
  <HelloWorld />
  <button @click="inc">Clicked {{ count }} times.</button>
</template>

<script lang="ts">
import { ref } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  components: {
    HelloWorld,
  },
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
}
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
