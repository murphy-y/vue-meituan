<template>
  <div class="m-life">
    <el-row>
      <ul class="nav">
        <li>
          <router-link to="/" class="takeout">美团外卖</router-link>
        </li>
        <li>
          <router-link to="/">猫眼电影</router-link>
        </li>
        <li>
          <router-link to="/" class="takeout">美团酒店</router-link>
        </li>
        <li>
          <router-link to="/" class="apartment">民宿／公寓</router-link>
        </li>
        <li>
          <router-link to="/" class="business">商家入驻</router-link>
        </li>
        <li>
          <router-link to="/">美团公益</router-link>
        </li>
      </ul>
    </el-row>
    <el-row>
      <el-col :span="14">
        <my-slider />
      </el-col>
      <el-col :span="4">
        <div class="m-life-pic">
        </div>
      </el-col>
      <el-col :span="6" >
        <div class="m-life-login">
          <h4><img src="//s0.meituan.net/bs/fe-web-meituan/e350c4a/img/avatar.jpg" alt=""></h4>
          <p class="m-life-login-name">Hi！
            {{$store.state.userName ? $store.state.userName : '你好'}}</p>
          <p v-if="!$store.state.userName"><router-link
            :to="{name: 'register'}" >
              <el-button round>注册</el-button>
            </router-link></p>
          <p v-if="!$store.state.userName"><router-link
            :to="{name: 'register'}" >
              <el-button round>立即登录</el-button>
            </router-link></p>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="7">
        <router-link to="/"><div class="m-life-hotel"></div></router-link>
      </el-col>
      <el-col :span="7">
        <router-link to="/"><div class="m-life-music"></div></router-link>
      </el-col>
      <el-col :span="4">
        <router-link to="/"><div class="m-life-coop"></div></router-link>
      </el-col>
      <el-col :span="6">
        <div class="m-life-downapp">
          <img src="//s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png" alt="">
          <p>美团APP手机版</p>
          <div class="last-p">
            <span>1元起</span>
            吃喝玩乐
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import MySlider from './slider.vue'
export default {
  components: {
    MySlider
  }
}
</script>

<style lang="scss">
  @import "@/assets/css/index/life.scss"
</style>
