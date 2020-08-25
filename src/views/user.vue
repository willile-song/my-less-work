<template>
    <div class="user">
        <el-button type="primary" @click="hanleClick">跳转</el-button>
        {{this.$route.params.id}}
    </div>
</template>
<script>
export default {
    watch: {
        $route(to, from) {
            console.log(to, from);
        }
    },
    methods: {
        hanleClick() {
            const param = this.$route.params.id == 1 ? 2 : 1;
            this.$router.push(`/user/${param}`);
        }
    },
    mounted() {
        console.log(11);
    }
};
</script>
<style lang="less" scoped>
.user {
    /deep/ .el-button {
        background-color: greenyellow;
    }
}
</style>