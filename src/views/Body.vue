<template>
  <div class="body">
    <div class="wrapper">
      <Header />
      <router-view />
    </div>
    <Footer />
    <!-- <Preloader v-if="this.$apollo.loading" :item="'cube-grid'" /> -->
  </div>
</template>

<script>
import Header from "@/components/Header/Header"
import Footer from "@/components/Footer/Footer"
// import Preloader from "../components/SmallBlocks/preloader"

export default {
  name: "app",
  components: {
    Header,
    Footer
    // Preloader
  }
}
</script>

<style lang="sass">
.body
  display: flex
  flex-direction: column
  height: 100%
  overflow-x: hidden
  .wrapper
    flex: 1 0 auto
  .footer
    flex-shrink: 0
</style>
