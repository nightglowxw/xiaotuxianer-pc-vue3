<template>
  <nav><AppTopnav /></nav>
  <header><AppHeader /></header>
  <main>
    <!-- 二级路由 -->
    <router-view></router-view>
  </main>
  <footer><AppFooter /></footer>
</template>

<script>
import AppTopnav from '@/components/app-topnav'
import AppHeader from '@/components/app-header'
import AppFooter from '@/components/app-footer'
export default {
  name: 'xtx-layout',
  components: { AppTopnav, AppHeader, AppFooter }
}
</script>

<style scoped lang="less">
main {
  min-height: 600px;
}
</style>
