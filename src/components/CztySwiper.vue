<!-- 本示例未包含完整css，获取外链css请参考上文，在hello uni-app项目中查看 -->
<script>
export default {
  data() {
    return {
      background: ['color1', 'color2', 'color3'],
      indicatorDots: true,
      autoplay: true,
      interval: 20000,
      duration: 100,
    };
  },
  methods: {
    changeIndicatorDots(e) {
      this.indicatorDots = !this.indicatorDots;
    },
    changeAutoplay(e) {
      this.autoplay = !this.autoplay;
    },
    intervalChange(e) {
      this.interval = e.target.value;
    },
    durationChange(e) {
      this.duration = e.target.value;
    },
  },
};
</script>

<!-- 本示例未包含完整css，获取外链css请参考上文，在hello uni-app项目中查看 -->
<template>
  <view>
    <view class="uni-margin-wrap">
      <swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
        <swiper-item>
          <img src="../img/20240305152358.jpg" alt="" />
        </swiper-item>
        <swiper-item>
          <img src="../img/20240305152321.jpg" alt="" />
        </swiper-item>
        <swiper-item>
          <!-- <view class="swiper-item uni-bg-blue">C</view> -->
          <img src="../img/20240305152348.jpg" alt="" />
        </swiper-item>
      </swiper>
    </view>
  </view>
</template>

<style>
.uni-margin-wrap {
  width: 690rpx;
  width: 100%;
}
.swiper {
  height: 450rpx;
}
.swiper-item {
  display: block;
  height: 300rpx;
  line-height: 300rpx;
  text-align: center;
}
.swiper-list {
  margin-top: 40rpx;
  margin-bottom: 0;
}
.uni-common-mt {
  margin-top: 60rpx;
  position: relative;
}
.info {
  position: absolute;
  right: 20rpx;
}
.uni-padding-wrap {
  width: 550rpx;
  padding: 0 100rpx;
}
</style>
