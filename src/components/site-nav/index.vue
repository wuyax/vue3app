<template>
  <header
    class="navbar fixed top-0 left-0 right-0 z-20 h-14 bg-white box-border border-b border-slate-300 flex items-center">
    <div class="sidebar-button cursor-pointer w-5 h-5 p-2 box-content md:hidden"
      @click="toggle">
      <svg xmlns="http://www.w3.org/2000/svg"
        aria-hidden="true"
        role="img"
        viewBox="0 0 448 512"
        class="icon">
        <path fill="currentColor"
          d="M436 124H12c-6.627 0-12-5.373-12-12V80c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12z">
        </path>
      </svg>
    </div>
    <div v-if="data.isOpenNav"
      class="sidebar fixed top-14 left-0 bottom-0 bg-white w-60 border-r border-slate-200 flex flex-col md:static md:border-r-0 md:bg-transparent md:w-auto md:flex-row">
      <img src=""
        alt="logo"
        srcset="">
      <nav class="flex flex-col md:inline-block">
        <router-link tag="a"
          class="block px-4 py-2 md:inline"
          to="/">首页</router-link>
        <router-link tag="a"
          class="block px-4 py-2 md:inline"
          to="/product">产品</router-link>
        <router-link tag="a"
          class="block px-4 py-2 md:inline"
          to="/server">服务</router-link>
        <router-link tag="a"
          class="block px-4 py-2 md:inline"
          to="/about">关于我们</router-link>
        <router-link tag="a"
          class="block px-4 py-2 md:inline"
          to="contact">联系我们</router-link>
      </nav>
    </div>

  </header>
</template>
<script setup>
import { ref, reactive } from 'vue'
const name = 'SiteNav'
const data = reactive({
  isOpenNav: false,
})
function toggle() {
  console.log('isOpenNav.value = ', data.isOpenNav)
  data.isOpenNav = !data.isOpenNav
}
</script>
<style lang="scss" scoped>
.navbar {
  padding: 0.7rem 1.5rem;
  line-height: 2.2rem;
}
</style>