<template>
  <nav><AppTopnav /></nav>
  <header>
    <AppHeader />
    <!-- 吸顶头部 -->
    <AppHeaderSticky />
  </header>
  <main>
    <!-- 二级路由 -->
    <router-view></router-view>
  </main>
  <footer><AppFooter /></footer>
</template>

<script>
import { useStore } from 'vuex'
import AppTopnav from '@/components/app-topnav'
import AppHeader from '@/components/app-header'
import AppFooter from '@/components/app-footer'
import AppHeaderSticky from '@/components/app-header-sticky'
export default {
  name: 'xtx-layout',
  components: { AppTopnav, AppHeader, AppFooter, AppHeaderSticky },
  // 获取下分类数据
  setup() {
    const store = useStore()
    store.dispatch('category/getList')
  }
}
</script>

<style scoped lang="less">
main {
  min-height: 900px;
}
</style>
