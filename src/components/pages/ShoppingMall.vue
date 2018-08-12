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
    </div>
</template>

<script>
/* eslint-disable */
export default {
  data() {
    return {
      msg: "value",
      locationIcon:require('../../assets/images/locate.svg')
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
</style>

