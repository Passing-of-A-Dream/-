<template>
  <div>
    <van-swipe :autoplay="3000" class="my-swipe">
      <van-swipe-item v-for="(image, index) in images" :key="index">
        <img v-lazy="image" />
      </van-swipe-item>
    </van-swipe>
  </div>
</template>

<script>
import Vue from "vue";
import { Lazyload } from "vant";
import { Swipe, SwipeItem } from 'vant';
Vue.use(Lazyload);
Vue.use(Swipe);
Vue.use(SwipeItem);
export default {
  name: "Boom",
  props: ["cont"],
  data() {
    return {
      images: [
        "http://www.taoyuanju.top/uploads/attach/2021/02/20210220/dcd4de24cfc4930636d994b33b3e5a68.jpg",
        "http://www.taoyuanju.top/uploads/attach/2021/01/20210107/fe6fcaec0e0a5608d36292a2097c0c47.jpg",
        "http://www.taoyuanju.top/uploads/attach/2021/01/20210114/b4ae224140c1b8508f32c0d2293f760f.jpg",
      ],
    };
  },
  components: {
    [Swipe.name]: Swipe,
    [SwipeItem.name]: SwipeItem,
  },
};
</script>
<style lang="scss" scoped>
.my-swipe .van-swipe-item {
  color: #fff;
  font-size: 20px;
  line-height: 150px;
  text-align: center;
  height: 26vh;
  // background-color: #39a9ed;
  border-radius: 5px;
  img{
    max-width: 100%;
  }
}
</style>