<template>
  <v-app>
    <!-- drawer menu -->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      :disable-resize-watcher="true"
      right
      fixed
      app
      color="black"
    >
      <v-list>
        <v-list-item router to="/" exact>
          <v-list-item-title class="d-flex justify-center"><p class="white--text drawer-list">Home</p></v-list-item-title>
        </v-list-item>
        <v-list-item router to="/menu" exact>
          <v-list-item-title class="d-flex justify-center"><p class="white--text drawer-list">Menu</p></v-list-item-title>
        </v-list-item>
        <v-list-item router to="/contact" exact>
          <v-list-item-title class="d-flex justify-center"><p class="white--text drawer-list">Contact</p></v-list-item-title>
        </v-list-item>
        <!-- <v-list-item router to="/slide" exact class="nav-slide">
          <v-list-item-title class="d-flex justify-center"><p class="white--text drawer-list">スライド</p></v-list-item-title>
        </v-list-item> -->
      </v-list>
    </v-navigation-drawer>

    <!-- nav bar -->
    <v-app-bar :clipped-right="clipped" fixed app color="black">
      <v-toolbar-items class="nav-bar">
        <v-toolbar-title class="white--text d-flex align-center">
          <nuxt-link to="/" tag="p" class="white-text nav-title">{{title}}</nuxt-link>
        </v-toolbar-title>
        <v-spacer />
        <v-toolbar-items class="d-none d-sm-block">
          <v-btn to="/menu" text class="white--text" style="text-transform: none">Menu</v-btn>
          <v-btn to="/contact" text class="white--text" style="text-transform: none">Contact</v-btn>
          <!-- <v-btn to="/slide" class="primary">スライド</v-btn> -->
        </v-toolbar-items>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="white--text d-sm-none"/>
      </v-toolbar-items>
    </v-app-bar>

    <!-- main -->
    <v-main>
      <Nuxt />
    </v-main>

    <!-- footer -->
    <v-footer :absolute="fixed" app color="black" class="d-flex justify-center">
      <span class="white--text text-center">&copy; {{ new Date().getFullYear() }}  Kamino Hajime All rights recerved.</span>
    </v-footer>
  </v-app>
</template>

<style scoped lang="scss">
.nav-bar {
  width: 1100px;
  margin: 0 auto;
  font-family: 'Cardo';
}
.drawer-list{
  font-family: 'Cardo';
  margin: 20px;
}
.nav-title{
  color: white;
  cursor: pointer;
  font-size: 28px;
  margin-bottom: 0;
}
.nav-slide{
  background-color: #1B77D2;
}
</style>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      clipped: true,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Sample Bar",
    };
  },
  methods:{
    // 600px以上でドロワーメニューを非表示
    drawerMenuShow(){
      if(window.outerWidth >= 600){
        this.drawer = false
      }
    }
  },
  mounted: function () {
    window.addEventListener('resize', this.drawerMenuShow)
  },
};
</script>
