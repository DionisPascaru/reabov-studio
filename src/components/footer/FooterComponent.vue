<template>
  <div class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="logo">
          <img src="@/assets/logo.svg" alt="logo">
        </div>
        <div class="footer-menu">
          <el-menu class="navigation-bar-menu"
                   background-color="transparent">
            <el-menu-item index="1" @click="goToSection('AboutRef')">About</el-menu-item>
            <el-menu-item index="2" @click="goToSection('PortfolioRef')">Portfolio</el-menu-item>
            <el-menu-item index="4" @click="goToSection('StockRef')">Stock</el-menu-item>
            <el-menu-item index="3" @click="goToSection('SocialRef')">Social</el-menu-item>
            <el-menu-item index="5" @click="goToSection('ContactRef')">Contact</el-menu-item>
          </el-menu>
        </div>
      </div>
      <copyright-component></copyright-component>
    </div>
  </div>
</template>

<script>
import CopyrightComponent from '../footer/CopyrightComponent.vue';

export default {
  name: 'FooterComponent',
  components: {
    CopyrightComponent
  },
  methods: {
    goToSection(value) {
      const top = document.getElementById(value).offsetTop;
      window.scrollTo({
        top: top - 132,
        left: 0,
        behavior: 'smooth'
      });
    },
  }
}
</script>