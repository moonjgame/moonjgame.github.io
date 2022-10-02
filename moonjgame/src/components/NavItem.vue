<template>
  <div id="navItem">
    <div class="navItem">
      <div class="logo">
        <img class="logeImg" src="../assets/logo.png" alt="" />
        <h1 class="logoText">月钩游戏</h1>
      </div>
      <div style="width: 640px">
        <!-- <div class="line"></div> -->
        <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="transparent"
          text-color="#fff"
          active-text-color="#ffd04b"
        >
          <!-- <el-menu-item index="1">首页</el-menu-item> -->
          <el-menu-item index="2">隐私政策</el-menu-item>
        </el-menu>
      </div>
      <div class="sign"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavItem",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
    };
  },
  methods: {
    handleSelect(key) {
      if (key == 1) {
        // this.router.push('home')
        // this.$router.push('/');
        //编程式导航
        this.$router.push(
          {
            name: "home",
          },
          () => {},
          () => {}
        );
        //添加 ()=>{},()=>{} 解决此问题
      } else if (key == 2) {
        // this.$router.push('/privacy');
        // this.router.push('privacy')

        this.$router.push(
          {
            name: "privacy",
          },
          () => {},
          () => {}
        );
      }
    },
  },
};
</script>


<style>
#navItem {
  margin: 0;
  padding: 0;
  background-color: #c77ad3;
}
.navItem {
  width: 1200px;
  margin: auto;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.logoText {
  padding: 0;
  margin: 0;
  font-size: 23px;
  color: antiquewhite;
}

.el-menu.el-menu--horizontal {
  border: none;
}
.logo {
  height: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 150px;
}
.logeImg {
  height: 50px;
  display: block;
}
.sign {
  width: 200px;
}
</style>