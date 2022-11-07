<script>
export default {
  data() {
    return {
      rndImg: "https://picsum.photos/800/500",
      myImg: "myimg.jpg",
    };
  },
  methods: {
    getImagePath: function () {
      return new URL(`../assets/${this.myImg}`, import.meta.url).href;
    },
  },
};
</script>
<template>
  <div>
    <img :src="rndImg" alt="" />
    <img :src="getImagePath()" alt="" />
  </div>
</template>
<style>
div {
  width: 100%;
  height: 500px;
  margin: 0 auto;
  border-radius: 10px;
  overflow: hidden;
}
img {
  width: 50%;
  object-fit: cover;
  height: 100%;
}
</style>
