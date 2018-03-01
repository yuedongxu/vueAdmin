<template>
  <div class="bg">
    <div class="login">
        <div class="title"><span>Admin</span><strong>管理系统</strong></div>
        <el-form>
            <el-input class="username inputBlock" v-model="username" placeholder="请输入用户名"></el-input>
            <el-input class="password inputBlock" type="password" v-model="password" placeholder="请输入密码">
              
            </el-input>


        </el-form>
        <el-button class="btn" @click="login">登录</el-button>
  </div>
  </div>
  
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      username: 'admin',
      password:'123456',
    }
  },
  methods:{
    login:function(){
        this.$router.push({path:'/home'})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
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
.bg{
    position:relative;
    width: 100%;
    height: 100%;
    background: #eee;
    overflow: hidden;
}
.login{
    width: 554px;
    height: 356px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    background: #fff;
    border-radius: 6px;
    overflow: hidden;
    z-index: 2;
  .title{
      height: 100px;
      line-height: 100px;
      font-size: 28px;
      span{
          color:#0094c2
      }
    
  }
  .btn{
    margin-top:20px;
    width:60%;
  }

}

.inputBlock{
    width: 60%;
    margin-bottom: 20px;
}
</style>
