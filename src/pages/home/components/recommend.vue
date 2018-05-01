<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <router-link tag="li"
          class="item border-bottom"
          v-for="item in list"
          :key="item.id"
          :to="'/detail/' + item.id"
          >
          <img :src="item.imgUrl" class="item-img">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top .2rem
  line-height .8rem
  background #eee
  text-indent .2rem
.item
  display flex
  height 2.2rem
  overflow hidden
  .item-img
    width 2rem
    height 2rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    position relative
    min-width 0
    .item-title
      line-height .54rem
      font-size .36rem
      ellipsis()
    .item-desc
      margin-top .2rem
      line-height .3rem
      font-size .26rem
      ellipsis()
    .item-button
      line-height .44rem
      padding 0 .2rem
      background #ff9300
      color $white
      margin-top .5rem
      font-size .3rem
      border-radius .06rem
</style>
