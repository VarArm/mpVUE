<template>
  <div class="mybox">
    <div class="list" v-for="(item,index) in datalist" :key="index">
      <a :href="'/pages/item/main?id='+item.id">
        <img :src="item.iconUrl" alt />
        <p>{{item.name}}</p>
      </a>
    </div>
  </div>
</template>

<script>
import datalist from "../../utils/lol_duowan";
export default {
  data() {
    return {
      datalist: datalist
    };
  }
};
</script>

<style scoped lang='less'>
.mybox {
  width: 100%;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
}
.list {
  width: 33.33%;
  text-align: center;
  a {
    width: 100%;
    height: 100%;
  }
  img {
    width: 100px;
    height: 100px;
  }
}
</style>
