<script>
import TabItem from "./components/TabItem.vue";
import TabBar from './components/TabBar.vue';
export default {
  components: {
    'TabItem': TabItem, //注册
    'TabBar':TabBar
  }
};
</script>

<template>
  <div>
    <router-view></router-view>
    <TabBar>
      <!--自定义path属性，用于传值.和TabItem.vue中props对应   textColor用于传递文本颜色-->
      <TabItem path="/home" textColor="pink">
        <template v-slot:item-img>
          <img src="./assets/imgs/tabBar/index.svg" />
        </template>
        <template v-slot:item-img-selected>
          <img src="./assets/imgs/tabBar/index-selected.svg" />
        </template>
        <template v-slot:item-title>
          <div>首页</div>
        </template>
      </TabItem>

      <TabItem path="/course" textColor="pink">
        <template v-slot:item-img>
          <img src="./assets/imgs/tabBar/course.svg" />
        </template>
        <template v-slot:item-img-selected>
          <img src="./assets/imgs/tabBar/course-selected.svg" />
        </template>
        <template v-slot:item-title>
          <div>课程</div>
        </template>
      </TabItem>

      <TabItem path="/friends" textColor="pink">
        <template v-slot:item-img>
          <img src="./assets/imgs/tabBar/friends.svg" />
        </template>
        <template v-slot:item-img-selected>
          <img src="./assets/imgs/tabBar/friends-selected.svg" />
        </template>
        <template v-slot:item-title>
          <div>朋友圈</div>
        </template>
      </TabItem>

      <TabItem path="/study" textColor="pink">
        <template v-slot:item-img>
          <img src="./assets/imgs/tabBar/study.svg" />
        </template>
        <template v-slot:item-img-selected>
          <img src="./assets/imgs/tabBar/study-selected.svg" />
        </template>
        <template v-slot:item-title>
          <div>学习</div>
        </template>
      </TabItem>

      <TabItem path="/my" textColor="pink">
        <template v-slot:item-img>
          <img src="./assets/imgs/tabBar/my.svg" />
        </template>
        <template v-slot:item-img-selected>
          <img src="./assets/imgs/tabBar/my-selected.svg" />
        </template>
        <template v-slot:item-title>
          <div>我的</div>
        </template>
      </TabItem>
    </TabBar>
  </div>
</template>

<style>
</style>
