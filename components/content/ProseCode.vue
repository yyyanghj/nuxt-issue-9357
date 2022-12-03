<script setup lang="ts">
defineProps({
  code: {
    type: String,
    default: '',
  },
  language: {
    type: String,
    default: null,
  },
  filename: {
    type: String,
    default: null,
  },
  highlights: {
    type: Array as () => number[],
    default: () => [],
  },
})
</script>

<template>
  <div class="shiki bg-neutral-50 dark:bg-neutral-900 my-4 mx-auto rounded-lg">
    <slot></slot>
  </div>
</template>

<style lang="postcss">
.shiki {
  overflow-x: auto;
  overflow-x: overlay;
  border-width: 2px;
  padding: 16px !important;

  .line {
    display: block;
    height: 20px;
    line-height: 20px;
  }

  > pre {
    margin: 0;
  }
}
</style>
