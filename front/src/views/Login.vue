<template>
  <div class="container">
    <div style="width: 25%; display: flex;background-color: white; ">


      <div style="flex: 1;width: 50%;padding: 40px;display: flex;flex-direction: column;justify-content: center;" >
        <div style="text-align: center; font-size: 28px;   color: #000000 ;margin-top: 10px;  ">校园宿舍管理系统</div>
        <el-form ref="form" :model="form" :rules="rules" size="large">
          <el-form-item prop="username">
            <el-input v-model="form.username" clearable prefix-icon="avatar"></el-input>
          </el-form-item>
          <el-form-item prop="password">
            <el-input v-model="form.password" prefix-icon="lock" show-password></el-input>
          </el-form-item>
          <el-form-item :model="form" prop="identity" style="margin-left: 2%;font-size: 30px!important;">
            <el-radio v-model="form.identity" label="stu" style="color: grey">学生</el-radio>
            <el-radio v-model="form.identity" label="dormManager" style="color: grey">宿舍管理员</el-radio>
            <el-radio v-model="form.identity" label="admin" style="color: grey">系统管理员</el-radio>
          </el-form-item>
          <el-form-item>
            <el-button :disabled="!disabled" style="width: 20%;height:40px ;background-color: #009DFFFF" @click="login">登 录</el-button>
          </el-form-item>
        </el-form>
      </div>

    </div>

  </div>

</template>
<script src="@/assets/js/Login.js"></script>
<style scoped>
@import '../assets/css/Login.css';
/deep/ .el-input--large{
  margin-top: 30px;     
}
/deep/ .el-button{
  width: 100%!important;
  background-color: #96463D;
  color: white;
  border: none;
  font-size: 20px;
  margin-top: 10px; 
}

.el-radio /deep/ .el-radio__label{

font-size:16px !important; 
 

}
.container {
  height: 100vh;
  overflow: hidden;
  /*background-color: #ff6427;*/
  background-image: url("../assets/bg2.png");
  background-size: 100% 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #666;
}
</style>