<template>
  <div class="pc-x-countdown" element-path="pc/x-countdown">
  {{viewModel}}
  </div>
</template>

<script>
  export default {
    name: 'x-countdown',
    props: {
      elementData: {}
    },
    data () {
      return {
        viewModel: ''
      }
    },
    mounted () {
      this.init()
    },
    methods: {
      async init () {
        if (this.elementData !== undefined) {
          this.viewModel = this.elementData
        }
      }
    }
  }
</script>

<style lang="less">
  @import '~_style/index.less';
  .pc-x-countdown {
  	font-size: @font-size-base;
  }
</style>
