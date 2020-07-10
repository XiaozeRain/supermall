<template>
  <tab-bar>
    <tab-bar-item linkurl="/home" activeColor="blue">
      <img slot="icon-img" src="~assets/img/tabbar/1.png" />
      <img slot="icon-img-act" src="~assets/img/tabbar/2.png" />
      <div slot="icon-text">首页</div>
    </tab-bar-item>
    <tab-bar-item linkurl="/cart" activeColor="green">
      <img slot="icon-img" src="~assets/img/tabbar/1.png" />
      <img slot="icon-img-act" src="~assets/img/tabbar/2.png" />
      <div slot="icon-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item linkurl="/category" activeColor="orange">
      <img slot="icon-img" src="~assets/img/tabbar/1.png" />
      <img slot="icon-img-act" src="~assets/img/tabbar/2.png" />
      <div slot="icon-text">分类</div>
    </tab-bar-item>
    <tab-bar-item linkurl="/profile">
      <img slot="icon-img" src="~assets/img/tabbar/1.png" />
      <img slot="icon-img-act" src="~assets/img/tabbar/2.png" />
      <div slot="icon-text">个人</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from "components/common/tabbar/TabBar";
import TabBarItem from "components/common/tabbar/TabBarItem";

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem
  }
};
</script>

<style scoped>
</style>