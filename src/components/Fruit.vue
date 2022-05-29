<template>
  <li>{{ name }}!!</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped lang="scss">
//scoped 현재 컴포넌트만 적용됨
  h1 {
    color: red !important;
  }
</style>