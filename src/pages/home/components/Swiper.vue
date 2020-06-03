<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
          <swiper-slide v-for="(item, index) in swiperList" :key="index">
            <img class="swiper-img" :src="item.imgUrl"/>
          </swiper-slide>
          <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1507/82/06e79c5f8d6e7.jpg_r_640x214_5e63707e.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/d1/3070ad726f861b.jpg_r_640x214_39709b85.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width 100%
    height 0
    padding-bottom 37.3%
    background #eee
    .swiper-img
      width: 100%
</style>
