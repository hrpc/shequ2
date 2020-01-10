<template>
  <div ref="main" class="main">
    <div>
      <div v-for="(item, index) in list" :key="index" class="main-item"></div>
    </div>
  </div>
</template>
<script>
import BScroll from '@better-scroll/core'
export default {
  props: {
    list: {
      type: Array,
      default: () => {
        return []
      }
    }
  },
  mounted () {
    /* eslint-disable no-new */
    new BScroll(this.$refs.main, {
      // ...... 详见配置项
    })
  }
}
</script>
<style scoped lang="stylus">
.main
  background-color $elsecolor
  height ceil($pageHeight - $headerHeight - $footerHeight)
  overflow hidden
  .main-item
    height 75px
    border-bottom 1px solid #d3d3d3
</style>
