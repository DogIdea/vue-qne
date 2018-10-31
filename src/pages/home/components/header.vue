<!--  -->
<template>
  <div class="header">
      <div class="header-left">
          <div class="iconfont icon-fanhui icon-back"></div>
      </div>
      <div class="header-input">
        <span class="iconfont icon-sousuo"></span>
         输入城市/景点/游玩主题
      </div>
      <router-link to='/city'>
        <div class="header-right">
          {{this.city}}
         <span class="iconfont icon-jiantouarrow486 arrow-icon"></span>
        </div>
      </router-link>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])
  }
}
</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.header
    display:flex
    line-height:$headerHeight
    height:$headerHeight
    background:$bgColor
    color:#fff
    .header-left
        width .64rem
        float:left
        height:.86rem
        .icon-back
            height:$headerHeight
            font-size:.4rem
            text-align:center
    .header-input
        flex:1
        color:#ccc
        background:#fff
        border-radius:.1rem
        margin-top:.12rem
        line-height:.64rem
        height:.64rem
        margin-left:.1rem
        padding-left:.2rem
    .header-right
        min-width:1.04rem
        float:right
        padding:0 .1rem
        text-align:center
        color:#fff
        .arrow-icon
            font-size:.24rem
</style>
