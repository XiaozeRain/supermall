<template>
  <div class="tab-bar-item" @click="onClickItem">
    <div v-if="!isActive">
      <slot name="icon-img"></slot>
    </div>
    <div v-else>
      <slot name="icon-img-act"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="icon-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    linkurl: {
        type:String,
        default:''
    },
    activeColor:{
        type:String,
        default:'red'
    }
  },
  data() {
    return {
      
    };
  },
  computed: {
      isActive(){
        //   console.log("this.$route.path",this.$route.path);
          return this.$route.path.indexOf(this.linkurl)!=-1;
      },
      activeStyle(){
          return this.isActive?{color:this.activeColor}:{}
      }
  },
  methods: {
    onClickItem() {
    //   this.isActive = !this.isActive;
    //   console.log(this.linkurl);
      this.$router.replace(this.linkurl).catch(err=>err);
    }
  }
};
</script>

<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  /* line-height: 49px; */
  font-size: 14px;
}

.tab-bar-item img {
  width: 24px;
  height: 24px;
  vertical-align: middle;
  margin: 3px;
}

</style>