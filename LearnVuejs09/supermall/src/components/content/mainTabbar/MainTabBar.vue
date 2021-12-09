<template>
  <tab-bar>
    <tab-bar-item path="/home" clickColor="deeppink">
      <img
        slot="item-icon-noClick"
        src="~assets/img/tabbar/homeNoClick.png"
        alt=""
      />
      <img
        slot="item-icon-click"
        src="~assets/img/tabbar/home.png"
        alt=""
      />
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/class" clickColor="green">
      <img
        slot="item-icon-noClick"
        src="~assets/img/tabbar/classNoClick.png"
        alt=""
      />
      <img
        slot="item-icon-click"
        src="~assets/img/tabbar/class.png"
        alt=""
      />
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/shopCar" clickColor="blue">
      <img
        slot="item-icon-noClick"
        src="~assets/img/tabbar/shopCarNoClick.png"
        alt=""
      />
      <img
        slot="item-icon-click"
        src="~assets/img/tabbar/shopCar.png"
        alt=""
      />
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/mine" clickColor="deeppink">
      <img
        slot="item-icon-noClick"
        src="~assets/img/tabbar/mineNoClick.png"
        alt=""
      />
      <img
        slot="item-icon-click"
        src="~assets/img/tabbar/mine.png"
        alt=""
      />
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from "./TabBar";
  import TabBarItem from "./TabBarItem";
  export default {
    name: "MainTabBar",
    components: {
      TabBar,
      TabBarItem
    }
  };
</script>

<style scoped></style>
