<template>
    <div>
        <div class="search-bar">
            <van-row>
             <van-col span="3">
                 <img :src="locationIcon" class="locate-icon" width="70%" alt="">
             </van-col>
             <van-col span="16">
                 <input type="text" class="search-input">
             </van-col>
             <van-col span="5">
                 <van-button class="btn-find" size="mini">
                      查找
                 </van-button>
             </van-col>
            </van-row>
        </div>

        <div class="swiper-area">
            <van-swipe :autoplay="3000">
                <van-swipe-item v-for="(banner,index) in bannerPicArray" :key="index">
                    <img v-lazy="banner.imageUrl" width="100%" alt="">
                </van-swipe-item>
            </van-swipe>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
export default {
  data() {
    return {
      msg: "value",
      locationIcon:require('../../assets/images/locate.svg'),
      bannerPicArray:[
          {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic001.jpg'},
          {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic002.jpg'},
          {imageUrl:'http://7xjyw1.com1.z0.glb.clouddn.com/simleVueDemoPic003.jpg'},
      ]
    };
  }
};
</script>

<style scoped>
.search-bar {
    height:2.2rem;
    padding-left:0.4rem;
    background: #e5017d;
    line-height: 2.2; 
    overflow: hidden;
}
.locate-icon {
    padding:0.2rem;
}
.search-input {
    width:100%;
    height: 1.3rem;
    border:0;
    border-bottom: 1px solid #fff !important;
    background: #e5017d;
    color: #fff !important;
}
.btn-find {
    margin-left:0.4rem;
}
.swiper-area{
      width:20rem;
      clear:both;
  }
</style>

