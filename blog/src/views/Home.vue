<template> 
  <div class="home">
    <el-row :gutter="150">
      <el-col :span="6"><div class="grid-content bg-purple">
    <iframe  class="bilibili" src="//player.bilibili.com/player.html?aid=3809649&bvid=BV1Ns41197kG&cid=6117915&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
  </div></el-col>
  <el-col :span="6"><div class="grid-content bg-purple">
    <span></span><br>
    <span></span><br>
    <span></span><br>
    <el-progress :percentage="50"></el-progress>
<el-progress :percentage="100" :format="format"></el-progress>
<el-progress :percentage="100" status="success"></el-progress>
<el-progress :percentage="100" status="warning"></el-progress>
<el-progress :percentage="50" status="exception"></el-progress>
</div></el-col>
</el-row>
<el-divider></el-divider>
<el-card class="box-card">博客推荐</el-card>
<el-button @click="drawer = true" type="primary" style="margin-left: 16px;">
  
  <i class="el-icon-video-play"></i>
</el-button>

<el-drawer
size
  title="音乐"
  :visible.sync="drawer"
  :with-header="false">
  
  <iframe class="music" frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=450 src="//music.163.com/outchain/player?type=0&id=2761182502&auto=1&height=430"></iframe>
</el-drawer>

    <div class="wrapper">
      
      <div class="main">
        <blog-list></blog-list>
      </div>
      
     
    
  </div>
    
  </div>

</template>

<script>
    // @ is an alias to /src
    import BlogList from "@/components/BlogList.vue";

    export default {
        name: "Home",
        components: {
            BlogList
        },
        data() {
            return {
                drawer: false,
            };
        },
        methods: {
            format(percentage) {
                return percentage === 100 ? '满' : `${percentage}%`;
            }
        }
    }
</script>

<style lang="scss" scoped>
    .el-row {
        margin-top: 20px;
        margin-bottom: 20px;
    }
    
    .bilibili {
        float: left;
        margin-left: 150px;
        width: 400px;
        height: 200px;
        border-radius: 10px;
    }
    
    .el-col {
        float: left;
        margin-left: 200px;
    }
    
    .el-progress {
        width: 250px;
        height: 30px;
    }
    
    .main {
        margin: 0 20px;
        padding: 20px;
        background: #f8f8fd;
        -webkit-box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4), 0 0 30px rgba(10, 10, 0, 0.1) inset;
        box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4), 0 0 30px rgba(10, 10, 0, 0.1) inset;
    }
    
    .el-button {
        position: fixed;
        left: -12px;
        top: 70%;
    }
    
    .el-card {
        height: 50px;
        width: 1160px;
        margin-bottom: 10px;
        margin-left: 50%;
        transform: translate(-50%);
        background: #2d2d2d;
        color: #9d9d9d;
        box-shadow: 0 2px 4px 1px rgba(0, 0, 0, 0.1);
    }
    
    .el-icon-video-play {
        font-size: large;
    }
</style>