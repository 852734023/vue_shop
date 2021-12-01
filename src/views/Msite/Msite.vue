<template>
  <div class="msite">
    <!--首页头部-->
     <HeaderTop title="松江区明泰苑">
         <span class="header_search" slot="left">
             <i class="iconfont icon-sousuo"></i>
         </span>
         <span class="header_login" slot="right">
             <span class="header_login_text">登录|注册</span>
         </span>
     </HeaderTop>

     <!--首页导航-->
     <nav class="msite_nav">
        <div class="swiper-container">
          <div class="swiper-wrapper">
              <div class="swiper-slide">
                <a href="javascript:">
                  <div class="food_container">
                    <img src="./images/003.jpg">
                  </div>
                  <span>BQBQ紫膜</span>
                </a>
              </div>
              <div class="swiper-slide">
                <a href="javascript:">
                  <div class="food_container">
                    <img src="./images/004.jpg">
                  </div>
                  <span>BQBQ红膜</span>
                </a>
              </div>
              <div class="swiper-slide">
                <a href="javascript:">
                  <div class="food_container">
                    <img src="./images/005.jpg">
                  </div>
                  <span>BQBQ赫柏青春女神系列</span>
                </a>
              </div>
              <div class="swiper-slide">
                <a href="javascript:">
                  <div class="food_container">
                    <img src="./images/006.jpg">
                  </div>
                  <span>BQBQ懒人霜</span>
                </a>
              </div>
              <div class="swiper-slide">
                <a href="javascript:">
                  <div class="food_container">
                    <img src="./images/007.jpg">
                  </div>
                  <span>BQBQ玫瑰花油</span>
                </a>
              </div>
          </div>
          <!-- 如果需要分页器 -->
          <div class="swiper-pagination"></div>
        </div>
      </nav>
      <!--首页附近商家-->
      <div class="msite_shop_list">
        <div class="shop_header"></div>
        <ShopList/>
      </div>
    <ShopList/>
  </div>
</template>

<script>
  import Swiper from 'swiper'
  import 'swiper/swiper.min.css'
  import HeaderTop from '../../components/HeaderTop/HeaderTop.vue'
  import ShopList from '../../components/ShopList/ShopList.vue'
  export default {
    mounted () {
      // 创建一个swiper实例对象，来实现轮播
      // eslint-disable-next-line no-new
      new Swiper('.swiper-container', {
        loop: true, // 循环模式选项
        // 如果需要分页器
        pagination: {
          el: '.swiper-pagination'
        }
      })
    },
    components: {
        HeaderTop,
        ShopList
    }
  }
</script>

<style lang="stylus" scoped>
  @import "../../common/stylus/mixins.styl"
  .msite
    width 100%
    .msite_nav
      bottom-border-1px(#e4e4e4)
      margin-top 45px
      height 180px
      background #fff
      .swiper-container
        width 100%
        height 100%
        .swiper-wrapper
          width 100%
          height 100%
          .swiper-slide
            display flex
            justify-content center
            align-items flex-start
            flex-wrap wrap
            .link_to_food
              width 25%
              .food_container
                display block
                width 100%
                text-align center
                padding 5px 0
                font-size 0
                img
                  display inline-block
                  width 50px
                  height 50px
              span
                display block
                width 100%
                text-align center
                font-size 12px
                color #666
        .swiper-pagination
          bottom 5px
          >span.swiper-pagination-bullet-active
              background #02a774

</style>
