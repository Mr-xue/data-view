<template>
  <div class="home">
      <dv-full-screen-container>
          <!--加载loading -->
          <dv-loading v-if="loading">Loading...</dv-loading>

          <div class="d-cont">
              <dv-border-box-1>dv-border-box-1</dv-border-box-1>
          </div>
      </dv-full-screen-container>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data() {
      return {
          loading : true,
      }
  },
  mounted() {
      setTimeout(()=>{
          this.loading = false;
      },1500)
  },
  components: {
  }
}
</script>

<style lang="less">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.home{
    position: absolute;
    width: 100%;
    height: 100%;
    background: url(../assets/bg.png);
    background-size: cover;
    background-position: 50% 50%;
}
#dv-full-screen-container{
    .d-cont{
        width: 100%;
        height: 100%;
        padding: 30px;
    }
    // 修改loading样式
    .dv-loading .loading-tip{
        color:#fff;
        font-weight: bold;
        font-size: 16px;
    }
}
</style>
