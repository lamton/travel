<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item in recommendList"
        :key="item.id">
        <img :src="item.imgUrl" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">评价</p>
          <p class="item-loc">{{item.location}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/8e/8e975801deb55d2fa3.water.jpg_200x200_ec0d5cd1.jpg',
          title: '李小龙乐园',
          location: '顺德区'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/8e/8e975801deb55d2fa3.water.jpg_200x200_ec0d5cd1.jpg',
          title: '李小龙乐园',
          location: '顺德区'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/8e/8e975801deb55d2fa3.water.jpg_200x200_ec0d5cd1.jpg',
          title: '李小龙乐园',
          location: '顺德区'
        },
        {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/8e/8e975801deb55d2fa3.water.jpg_200x200_ec0d5cd1.jpg',
          title: '李小龙乐园',
          location: '顺德区'
        }
      ]
    }
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
    .item-loc
      position absolute
      bottom .2rem
      right .2rem
    .item-button
      line-height .44rem
      padding 0 .2rem
      background #ff9300
      color #fff
      margin-top .5rem
      font-size .3rem
      border-radius .06rem
</style>
