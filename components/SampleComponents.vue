<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    <div>
      <button type="button" name="button" @click="plus">
        click times :{{ num }}
      </button>
    </div>
    <div :class="['hide', { seven: num === 7 }]">
      click 7 times
    </div>
    <div class="slot">
      <slot />
    </div>
    <!-- /.slot -->
    <div class="named">
      <slot name="named" />
    </div>
    <!-- /.named -->
  </div>
  <!-- /.sample -->
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title'
    }
  },
  data() {
    return {
      name: 'TrianglePlus',
      num: 0
    }
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}
</style>
