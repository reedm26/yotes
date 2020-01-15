<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,
      <br />check out the
      <a
        href="https://cli.vuejs.org"
        target="_blank"
        rel="noopener"
      >vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-router"
          target="_blank"
          rel="noopener"
        >router</a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-vuex"
          target="_blank"
          rel="noopener"
        >vuex</a>
      </li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a>
      </li>
      <li>
        <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a>
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a>
      </li>
      <li>
        <a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a>
      </li>
    </ul>
    <div ng-app="weatherApp" ng-controller="forecastController" class="component--weatherBox">
      <div class="panel">
        <div class="weather-data">
          <h1>{{ weather.city.name }}</h1>
          <small>{{ dailyForecast[0].weather[0].description }}</small>
        </div>
        <div class="currentTemp">
          <i ng-class="applyIcon(dailyForecast[0].weather[0].icon)" class="wi"></i>
          <i class="wi wi-degrees"></i>
        </div>
      </div>
      <div class="component--weatherBox-row">
        <div ng-repeat="daily in dailyForecast track by $index" class="content">
          <div class="component--weatherBox-heading">{{ day($index) }}</div>
          <div class="component--weatherBox-info">
            <i ng-class="applyIcon(daily.weather[0].icon)" class="wi"></i>
            <span class="degrees">
              {{ daily.temp.day | number: 0}}
              <i class="wi wi-degrees"></i>
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
