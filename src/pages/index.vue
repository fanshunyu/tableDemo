<template>
  <div class="index">
    <router-link to="el-data-table">Go2Table</router-link>
    <img class="home-img" :src="$store.state.meta.homePageImg" alt="homeImg" />
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {}
}
</script>
<style lang="less">
.index {
  .home-img {
    width: 100%;
  }
}
</style>