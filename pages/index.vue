<template>
  <div class="container">
    <div class="content-wrapper">
      <Header />
      <Main :list="contactInfoList" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Main from '@/components/Main.vue'
export default {
  components: {
    Header,
    Footer,
    Main
  },
  asyncData (context) {
    return {
      contactInfoList: new Array(20)
    }
  }
}
</script>

<style lang="stylus" scoped>
.container
  display flex
  align-items center
  justify-content center
  min-height 100vh
  .content-wrapper
    width $pageWidth
    height $pageHeight
    position relative
    background-color $mainbg
</style>
