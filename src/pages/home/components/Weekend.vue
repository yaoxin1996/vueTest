<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
          <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
            <div class="item-image-wrapper">
                <img class="item-img" :src="item.imgUrl">
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [{
        id: '0001',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/1af771fcad5f4501a55dfb6891b06886.jpeg_640x480x70_ac1b7eb4.jpeg',
        title: '阿尔卡迪亚御临泉温泉',
        desc: '让每一位前来的消费者感到《家》的氛围'
      }, {
        id: '0001',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/1af771fcad5f4501a55dfb6891b06886.jpeg_640x480x70_ac1b7eb4.jpeg',
        title: '阿尔卡迪亚御临泉温泉',
        desc: '让每一位前来的消费者感到《家》的氛围'
      }, {
        id: '0001',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/1af771fcad5f4501a55dfb6891b06886.jpeg_640x480x70_ac1b7eb4.jpeg',
        title: '阿尔卡迪亚御临泉温泉',
        desc: '让每一位前来的消费者感到《家》的氛围'
      }]
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
  .item-image-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
</style>
