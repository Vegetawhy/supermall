<template>
  <div class="tab-bar-item" @click="itemClick">
    <!-- <img src="../../assets/img/tabbar/home.png" alt="" />
    <div>首页</div> -->
    <div v-if="!isClick">
      <slot name="item-icon-noClick"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-click"></slot>
    </div>
    <!-- :class="{ isClick }" -->
    <div :style="clickStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    props: {
      // 父传子路径
      path: String,
      // 封装起来可在使用组件时动态传入颜色，不用修改封装好的组件
      clickColor: {
        type: String,
        default: "#ff4e4e"
      }
    },
    data() {
      return {
        // isClick: false,
      };
    },
    computed: {
      isClick() {
        // 判断当前活跃的路径是否包括当前传进来的路径
        return this.$route.path.indexOf(this.path) !== -1;
      },
      clickStyle() {
        return this.isClick ? { color: this.clickColor } : "";
      }
    },
    methods: {
      itemClick() {
        this.$router.push(this.path);
      }
    }
  };
</script>

<style scoped>
  .tab-bar-item {
    flex: 1;
    text-align: center;
    /* 49px是常用高度 */
    height: 49px;
    font-size: 14px;
    margin-top: 3px;
  }
  .tab-bar-item img {
    vertical-align: middle;
    height: 24px;
    width: 24px;
  }
  /* .isClick {
    color: #ff4e4e;
  } */
</style>
