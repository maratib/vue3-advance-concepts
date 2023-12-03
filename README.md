# Vue 3 Advance concepts

## Use Refs (instead of using DOM elements directly)
```javascript
<script setup lang="ts">
import { ref, onMounted } from 'vue'

const el = ref<HTMLInputElement | null>(null)

onMounted(() => {
  el.value?.focus()
})
</script>

<template>
  <input ref="el" />
</template>
```
## Slots

## Render h()
```javascript
<template>
    <render />
</template>

<script setup lang="ts">
import { h } from 'vue';
import Foo from '@/components/Foo.vue'
import Bar from '@/components/Bar.vue'


const render = () => {
  return h('div', [h(Foo), h(Bar)]) //Multiple elements
  // return h(Foo) //Single elements
}

</script>
```
## Add Dynamic classes to an element
```html
//Add class red if isError is true
<div :class=”{'red': isError}”></div>

// Add to classes if two properties return true
<div :class=" {'red': isError, 'text-bold': isActive }"></div>
```

