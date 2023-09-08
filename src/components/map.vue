<template>
  <div id="mapbox">
    <div id="mars3dContainer"></div>
  </div>
</template>
<script setup lang="ts">
import { onMounted } from "vue";
//引入cesium基础库
import * as mars3d from "mars3d";
import options from "./img/data-view-config.json";
// import "mars3d-cesium/Build/Cesium/Widgets/widgets.css";
function initmap() {
  var map = new mars3d.Map("mars3dContainer", options);
  console.log(map);
}
onMounted(() => {
  initmap();
});
</script>
<style lang="scss" scoped>
#mapbox {
  width: 100%;
  height: 100%;
  // overflow: hidden;
  // position: relative;
  // border: 1px solid red;
}
#mars3dContainer {
  width: 100%;
  height: 100%;
  // border: 1px solid yellow;
}
</style>
