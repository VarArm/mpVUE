<template>
  <div>item</div>
</template>

<script>
import heroitem from "../../utils/lol_details_duowan.js";
export default {
  data() {
    return {
      heroitem: heroitem,
      heroObj: {}
    };
  },
  mounted() {
    let id = this.$root.$mp.query.id;
    console.log(id);
    console.log(this.heroitem);

    this.heroObj = this.heroitem.filter(item => {
      return item.id === id;
    })[0];
    // this.heroObj = this.heroitem.filter(item => {
    //   return item.id === id;
    // })[0];
    console.log(this.heroObj);
  }
};
</script>

<style>
</style>
