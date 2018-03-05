<template>
    
    
<el-container style="height: 100%; border: 1px solid #eee;">
    <el-header style="font-size: 12px;background:#409EFF;">
        <el-row  type="flex" justify="space-between" style="height:60px">
            <div style="color:#fff;font-size:28px;">后台管理系统</div>
            <span>
                <el-dropdown style="height:30px;">
                    <i class="el-icon-setting" style="margin-right: 15px"></i>
                    <el-dropdown-menu slot="dropdown">
                      <el-dropdown-item>查看</el-dropdown-item>
                      <el-dropdown-item>修改</el-dropdown-item>
                      <el-dropdown-item>退出</el-dropdown-item>
                    </el-dropdown-menu>
                </el-dropdown>
                <span style="color:#fff;">admin</span>
            </span>
        </el-row>
        
        
    </el-header>
  
  
  <el-container>
    <el-aside width="200px" style="background-color: #eef1f6">
        <el-menu  :default-openeds="[]">
            <el-menu-item  index="1-1">
                <template slot="title"><i class="el-icon-menu"></i>首页</template>               
            </el-menu-item>
            <el-submenu index="2">
                <template slot="title"><i class="el-icon-message"></i>文章管理</template>
                <el-menu-item-group>
                    <template slot="title"></template>
                    <el-menu-item index="2-1">文章列表</el-menu-item>
                    <el-menu-item index="2-2">发布文章</el-menu-item>
                </el-menu-item-group>
            
            </el-submenu>
            <el-submenu index="3">
                <template slot="title"><i class="el-icon-document"></i>标签管理</template>
                <el-menu-item-group>
                  <template slot="title"></template>
                  <el-menu-item index="3-1">标签列表</el-menu-item>
                  <el-menu-item index="3-2">新增标签</el-menu-item>
                </el-menu-item-group>
            </el-submenu>
            <el-submenu index="4">
                <template slot="title"><i class="el-icon-setting"></i>友链管理</template>
                <el-menu-item-group>
                  <template slot="title"></template>
                  <el-menu-item index="4-1">友链列表</el-menu-item>
                </el-menu-item-group>
            </el-submenu>
        </el-menu>
    </el-aside>
    
    <el-main>
        <el-breadcrumb separator="/">
          <el-breadcrumb-item :to="{ path: '/home' }">首页</el-breadcrumb-item>
          <el-breadcrumb-item>活动管理</el-breadcrumb-item>
          <el-breadcrumb-item>活动列表</el-breadcrumb-item>
          <el-breadcrumb-item>活动详情</el-breadcrumb-item>
        </el-breadcrumb>
        <!-- <el-table :data="tableData">
        <el-table-column prop="date" label="日期" width="140">
        </el-table-column>
        <el-table-column prop="name" label="姓名" width="120">
        </el-table-column>
        <el-table-column prop="address" label="地址">
        </el-table-column>
        </el-table> -->
    </el-main>
  </el-container>
</el-container>
</template>
<style>
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }
  
  .el-aside {
    color: #333;
  }
</style>

<script>
  export default {
    data() {
      const item = {
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      };
      return {
        tableData: Array(20).fill(item)
      }
    }
  };
</script>