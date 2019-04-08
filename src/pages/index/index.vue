<template>
  <div @click="clickHandle">
    <i-notice-bar icon="systemprompt" loop>
    mt手帐上新啦！
    </i-notice-bar>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/1.png" />
        </i-grid-icon>
        <i-grid-label>和纸胶带</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/2.png" />
        </i-grid-icon>
        <i-grid-label>便签</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/3.png" />
        </i-grid-icon>
        <i-grid-label>贴纸</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/4.png" />
        </i-grid-icon>
        <i-grid-label>印章</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/5.png" />
        </i-grid-icon>
        <i-grid-label>书写工具</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/6.png" />
        </i-grid-icon>
        <i-grid-label>册本</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-panel title="店铺推荐">
      <view class="top-padding">
      <i-card title="雅皮士与棕熊" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">复古素材</view>
        <view slot="footer">店铺链接</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="靠近我温暖你" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">各种风格</view>
        <view slot="footer">店铺链接</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="Cool Patch" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">布贴</view>
        <view slot="footer">店铺链接</view>
      </i-card>
      <view class="top-padding"></view>
      <i-card title="南风手帐" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">jpg</view>
        <view slot="footer">店铺链接</view>
      </i-card>
      <view class="top-padding"></view>
    </view>
    </i-panel>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
.top-padding {
  padding-top: 50rpx;
}
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
