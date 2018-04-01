<template>
  <div id="app">
    <img src="./assets/logo.png">
    <el-row :gutter="20">
    <el-col :span="12">
      <el-input
              type="textarea"
              :autosize="{minRows:2,maxRows:20}"
              placeholder="Please input news article"
              v-model="textarea">
      </el-input>
    </el-col>
    <el-col :span="12">
      <p>{{message}}</p>
    </el-col>
    </el-row>
    <div>
      <el-button @click="startHacking">Start</el-button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }
  },
  data(){
    return{
        textarea: '',
        message:'success'
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
