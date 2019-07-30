<template>
  <div class="header">
    <div class="main">
      <el-row justify="space-between" type="flex">
        <!-- logo部分 -->
        <div class="logo">
          <img alt src="http://157.122.54.189:9093/images/logo.jpg">
        </div>
        <!-- logo部分结束 -->
        <!-- 菜单部分 -->
        <el-row class="menu" type="flex">
          <nuxt-link to="/">
            首页
          </nuxt-link>
          <nuxt-link to="/post">
            旅游攻略
          </nuxt-link>
          <nuxt-link to="/hotel">
            酒店
          </nuxt-link>
          <nuxt-link to="/air">
            机票
          </nuxt-link>
        </el-row>
        <!-- 菜单部分结束 -->
        <!-- 登录注册部分 -->
        <div v-if="false">
          <div class="login">
            <nuxt-link to="/user/login">
              登陆 / 注册
            </nuxt-link>
          </div>
        </div>
        <div v-else>
          <el-dropdown>
            <span class="el-dropdown-link">
              <img src="http://157.122.54.189:9095/assets/images/avatar.jpg" alt="">
              天青色等烟雨
              <i class="el-icon-arrow-down el-icon--right" />
            </span>
            <el-dropdown-menu slot="dropdown" style="width: 150px">
              <el-dropdown-item>个人中心</el-dropdown-item>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
        <!-- 登录注册部分结束 -->
      </el-row>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="sass" scoped>
.header
  height: 60px
  line-height: 60px
  border-bottom: 1px solid #ccc
  box-shadow: 0 3px 3px #eee
  .main
    width: 1000px
    margin: 0 auto
    .logo
      margin-top: 9px
      img
        width: 156px
        height: 42px
        display: block
    .menu
      flex: 1
      margin-left: 30px
      a
        display: block
        height: 60px
        line-height: 60px
        padding: 0 20px
        box-sizing: border-box
        &:hover
          color: #409eff
          border-bottom: 5px solid #409eff
      .nuxt-link-exact-active
        background: #409eff
        color: #fff
        &:hover
          color: #fff
  .login
    a
      &:hover
        color: #409eff
  .el-dropdown-link
    &:hover
      img
        border: 2px solid #409eff
        border-radius: 50%
    img
      width: 36px
      height: 36px
      vertical-align: middle
      margin-right: 8px
      border: 2px solid #fff
</style>
