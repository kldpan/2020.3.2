<template>
  <div class="home">
    <!-- 切换路由组件 -->
     <keep-alive>
          <router-view v-if="$route.meta.keepAlive" v-wechat-title="$route.meta.title" img-set="/img/favicon.ico" />
    </keep-alive>  
          <router-view v-if="!$route.meta.keepAlive" v-wechat-title="$route.meta.title" img-set="/img/favicon.ico" />

    <!-- 底部导航 -->
    <tabbar/>

  </div>
</template>

<script>

import tabbar from "@/components/layout/tabbar.vue";

export default {
  components:{
    tabbar
  }
};
</script>
