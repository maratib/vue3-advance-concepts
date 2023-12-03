<template>
  <div>
    <h1>Render 1</h1>
    <render />
  </div>
</template>

<script setup lang="ts">
import { h } from 'vue';
import Foo from '@/components/Foo.vue'
import Bar from '@/components/Bar.vue'


const render = () => {
  return h('div', [h(Foo), h(Bar)])
}

</script>

