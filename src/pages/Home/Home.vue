<template>
  <div>
    <search-bar></search-bar>
    <!-- 轮播图 -->
    <swiper   
        circular="true"     
        :indicator-dots="indicatorDots"
        :interval="interval"
        :duration="duration"
        :autoplay="autoplay">
      <swiper-item
        v-for="(item,index) in imgUrls"
        :key="index"
      >
        <image :src="item" class="slide-image"></image>
      </swiper-item>
    </swiper>
  </div>
</template> 

<script>
import SearchBar from "../../components/searchbar";
export default {
  components: {
    "search-bar": SearchBar
  },
  data() {
    return {
      imgUrls: [
        "https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640",
        "https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640",
        "https://images.unsplash.com/photo-1551446591-142875a901a1?w=640"
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 2000,
      duration: 1000
    };
  }
};
</script>

<style scoped>
.slide-image {
  width: 750rpx !important;
}
</style>
