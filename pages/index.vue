<template>
  <div>
    <sample-components :title="indexTitle">
      <div class="come">
        slot example
      </div>
      <div slot="named">
        named slot
      </div>
      <!-- /.come -->
    </sample-components>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
</template>

<script>
import SampleComponents from '~/components/SampleComponents.vue'

export default {
  components: {
    SampleComponents
  },
  data() {
    return {
      indexTitle: 'Nuxt.js Titles'
    }
  }
}
</script>

<style></style>
