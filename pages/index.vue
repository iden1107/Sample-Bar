<template>
  <div class="home">
    <section class="top">
      <div class="py-5 mx-auto d-flex align-center justify-center">
        <p class="white--text">Sample Bar</p>
      </div>
    </section>
    <section class="concept">
      <div class="container">
        <p class="white--text sub-title">Concept</p>
        <v-row>
          <v-col cols="12" sm="5">
            <img
              src="~@/assets/alcohol-g119c98c6d_1920.jpg"
              alt=""
              width="100%"
            />
          </v-col>
          <v-col cols="12" sm="7">
            <p class="white--text">
              このサイトはポートフォリオです。本サイトは架空であり、実在する人物、団体等とは一切関係ありません。写真はフリー画像素材<a href="https://pixabay.com/ja/" class="white--text">pixabay</a>、<a href="https://www.ac-illust.com/" class="white--text">illustAC</a>から引用しています。<br />
              このサイトはポートフォリオです。本サイトは架空であり、実在する人物、団体等とは一切関係ありません。写真はフリー画像素材<a href="https://pixabay.com/ja/" class="white--text">pixabay</a>、<a href="https://www.ac-illust.com/" class="white--text">illustAC</a>から引用しています。<br />
              このサイトはポートフォリオです。本サイトは架空であり、実在する人物、団体等とは一切関係ありません。写真はフリー画像素材<a href="https://pixabay.com/ja/" class="white--text">pixabay</a>、<a href="https://www.ac-illust.com/" class="white--text">illustAC</a>から引用しています。<br />
            </p>
          </v-col>
        </v-row>
      </div>
    </section>
    <section class="store">
      <div class="container">
        <p class="white--text sub-title">Store</p>
        <v-row>
          <v-col cols="12" sm="4">
            <p class="white--text text-center text-h5">新宿店</p>
            <img
              src="~@/assets/bar-g652964793_1920.jpg"
              alt=""
              width="100%"
            />
            <p class="white--text">東京都新宿区XX-XX</p>
          </v-col>
          <v-col cols="12" sm="4">
            <p class="white--text text-center text-h5">渋谷店</p>
            <img
              src="~@/assets/bar-g53473698e_1920.jpg"
              alt=""
              width="100%"
            />
            <p class="white--text">東京都渋谷区XX-XX</p>
          </v-col>
          <v-col cols="12" sm="4">
            <p class="white--text text-center text-h5">難波店</p>
            <img
              src="~@/assets/interior-g04a568cb0_1920.jpg"
              alt=""
              width="100%"
            />
            <p class="white--text">大阪府大阪市XX-XX</p>
          </v-col>
        </v-row>
      </div>
    </section>
    <section class="source">
      <div class="container">
        <p class="white--text sub-title">Source</p>
        <p class="white--text text-center">ソースコードは<a href="https://github.com/iden1107/Sample-Bar" target="_blank" class="white--text">こちら</a>のGithubで公開しています</p>
      </div>
    </section>
  </div>
</template>

<style scoped lang="scss">
.home{
  background-image: url("~@/assets/black-g73bfa2a23_1280.png");
  background-size: cover;
  background-attachment: fixed;
  height: 100%;
}
.container {
  max-width: 1100px;
  padding: 8vh 5vh 0vh;
}
img {
  margin: auto;
}
.sub-title{
  font-family: "Cardo";
  font-size: 40px;
  text-align: center;
}
.top {
  background-image: url("~@/assets/restaurant-g691fb34fb_1920.jpg");
  background-size: cover;
  background-position: center center;
  height: 40vh;
  display: flex;
  justify-content: center;
  p {
    font-family: "Cardo";
    font-size: 60px;
  }
}
</style>

<script>
export default {
  name: "IndexPage",
};
</script>
