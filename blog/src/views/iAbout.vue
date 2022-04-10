<template>
    <div class="allabout">
    <div class="main">
        <span class="guanyu">关于博客</span>
        <el-divider></el-divider>
        
      </div>
    <el-card class="box-card">
        <div>
        <div class="item">
          博客的意义在于分享
        </div>
        <div class="item">
          此个人博客为vue+element+node前后端分离的系统
        </div>
        <div class="item">
            可以浏览形形色色的博主发布的博客
          </div>
          <div class="item">
            登录and加入他们！
          </div>
    </div>
      </el-card>
    </div>
</template>

<script>
    export default {
        name: 'iabout'
    }
</script>

<style lang="scss" scoped>
    .allabout {
        height: 520px;
    }
    
    .main {
        text-align: center;
        margin: 20px auto;
    }
    
    .guanyu {
        font-size: 20px;
        color: aquamarine;
    }
    
    .item {
        font-size: 14px;
        padding: 18px 0;
    }
    
    .box-card {
        float: left;
        margin-left: 50%;
        transform: translate(-50%);
        width: 680px;
    }
</style>