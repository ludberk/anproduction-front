<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue'

// Import Swiper styles
import 'swiper/css'

import 'swiper/css/pagination'
import 'swiper/css/navigation'

// import required modules
import { Autoplay, Pagination, Navigation } from 'swiper/modules'

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation]
    }
  }
}
</script>
<template>
  <swiper
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false
    }"
    :pagination="{
      clickable: true
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide
      style="
        background-image: url('https://images.unsplash.com/photo-1689890076740-93e14bcae55b?q=80&w=1539&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
      "
    >
      <h1>Xəyalınızdakı Mebelin Hazırlanması -</h1>
    </swiper-slide>
    <swiper-slide
      style="
        background-image: url('https://images.unsplash.com/photo-1690022938772-e903dcd9a56e?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
      "
      ><h1>Mebellərin Hazırlanması -</h1></swiper-slide
    ><swiper-slide
      style="
        background-image: url('https://images.unsplash.com/photo-1624625870107-95b59a83967a?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
      "
      ><h1>Hər Növ Mebellərin Hazırlanması -</h1></swiper-slide
    >
  </swiper>
</template>
<style lang="less">
@import '../assets/base';
.swiper {
  width: 100%;
  height: 75vh;
}
.swiper-slide {
  .back-cover();
  .flex-y-center();
  .content {
    z-index: 10;
    margin: 10px;
  }
  h1 {
    color: #fff;
    font-size: 2.2rem;
  }
}
.overlay {
  position: absolute;
  width: 100%;
  height: 100vh;
  background-color: @transparent-dark;
  z-index: 1;
}
</style>
