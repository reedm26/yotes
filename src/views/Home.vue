<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
<style>
/* Variables */

/* Styles */
body {
  background: #dce2e5;
  font-family: "Roboto", sans-serif;
  font-weight: 100;
  font-size: 11px;
}
.component--weatherBox {
  margin: 30px auto;
  width: 420px;
  border: 1px solid darken(#81bdf4, 3%);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 2px 5px 20px 1px #444;
}

.panel {
  position: relative;
  overflow: hidden;
  color: #fff;
  background: #81bdf4;
  height: 120px;
  content: "";
  display: block;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  opacity: 0.3;
  background-image: url("https://nunnz.files.wordpress.com/2013/11/4.jpg");
  background-repeat: no-repeat;
  background-position: 0 63%;
  background-size: cover;
}

.weather-data {
  width: 50%;
  text-align: center;
  display: inline-block;
  float: left;
  z-index: 2;
  position: relative;
}

h1 {
  font-weight: 400;
  font-size: 40px;
  line-height: 40px;
  padding-bottom: 0;
  margin-bottom: 0;
  margin-top: 0.75em;
}

.currentTemp {
  width: 50%;
  z-index: 2;
  text-align: center;
  float: left;
  font-size: 50px;
  text-align: center;
  margin-top: 0.5em;
  position: relative;
  vertical-align: middle;
}
.degrees {
  line-height: 40px;
}
.wi-degrees {
  margin-left: -10px;
  vertical-align: top !important;
}
.wi {
  margin-right: 20px;
  font-size: 40px;
  vertical-align: baseline;
}
.component--weatherBox-row {
  display: flex;
  clear: both;
}

.content {
  flex: 1;
  text-align: center;
}

.component--weatherBox-heading {
  background: lighten(#81bdf4, 8%);
  border: 1px solid darken(#81bdf4, 10%);
  border-left: none;
  text-transform: uppercase;
  color: #fff;
  font-weight: 800;
  padding: 10px;
}

.component--weatherBox-info {
  background: #fff;
  color: #81bdf4;
  padding-bottom: 10px;
  border-right: 1px solid darken(#81bdf4, 10%);
}
.wi {
  display: block;
  margin: 0 auto;
  font-size: 24px;
  padding: 15px 0;
}
.degrees {
  font-size: 20px;
  line-height: 20px;
}
.wi-degrees {
  display: inline;
}

small {
  font-size: 12px;
}
</style>
