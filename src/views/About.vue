<template>
  <div class="about">
    <h1>This is an about page</h1>
    <el-button @click="handleClick">click</el-button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      infoList: [
        {
          name:'lina',
          age:22,
        },
        {
          name: 'dagu',
          age: 23,
        }
      ]
    }
  },
  methods: {
    handleClick() {
      this.infoList[2] = {
        name:'gesila',
        age:5000,
      },
      this.infoList.push({
        name: 'tailuo',
        age:4444,
      })
      console.log(this.infoList)
    }
  },
}
</script>

<style lang="less" scoped>
.about {
  h1{
    color:greenyellow;
  }
}
</style>>


