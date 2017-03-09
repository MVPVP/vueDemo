<!--App.vue是项目入口文件。-->
<template>
    <div id="app">
        <header-tab></header-tab>
        <h2>{{msg}}</h2>
        <div class="nav-box">
            <p class="nav-list">
                <router-link class="nav-item" to="/">首页</router-link>
                <router-link class="nav-item" to="/about">关于</router-link>
            </p>
        </div>
        <div>
            <router-view></router-view>
        </div>
    </div>
</template>

<script>
import HeaderTab from './components/header.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    HeaderTab
  }
}
</script>

<style lang="sass">
    /*这里sass编译正常*/
    $redColor:#f00;
    h2{
        color:$redColor;
    }
    #app {
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
    h1, h2 {
        font-weight: normal;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        text-align: left;
        margin: 0 10px;
    }
    a {
        color: #42b983;
    }
</style>
