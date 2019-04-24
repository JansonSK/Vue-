<template>
  <div id="app">
    <!-- index
    <el-button type="danger">危险按钮</el-button>
    <el-alert
      title="成功提示的文案"
      type="success">
    </el-alert> -->

    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',

  mounted(){
    // axios会返回promise对象，对象下面有then这方法
    this.$axios({
      // 路径
      url: "https://api.github.com/users",
      // 请求方式
      method: "GET",
      // get请求参数
      params: {},
    }).then(res => {
      console.log(res)
    })
  }
}
</script>

<style>

</style>
