<template>
  <div class="layout-wrapper" :class="classPrefix && `${classPrefix}-wrapper`">
    <div class="content" :class="classPrefix && `${classPrefix}-content`">
      <slot />
    </div>
    <Nav />
  </div>
</template>
<script lang="ts">
export default {
  props: ["classPrefix"],
  name: "Layout",
};
</script>

<style lang="scss" scoped>
.layout-wrapper {
  display: flex;
  // border: 1px solid green;
  flex-direction: column;
  min-height: 100vh;
}
.content {
  // border: 1px solid blue;
  overflow: auto;
  flex-grow: 1;
  height: 90vh;
}
</style>