<template>
    <div class="MyctiList">
        <div class="user">
            <img :src="user.headimgurl">
            <span>{{user.nickname}}</span>
        </div>

        <div style="margin-top: 2%">
            <van-cell title="我的参与" is-link to="ActivitiesDetails"/>
            <van-cell title="其他" is-link />
        </div>
<<<<<<< HEAD
=======

>>>>>>> c75b95803d391ab0c19be27eed7e4577727d8ad0
    </div>
</template>

<script>
    export default {
        name: "MyctiList",
        data(){
          return {
              user:[]//获取用户信息
            }
        },
        created:function () {
            //用户信息
            this.$axios.get(this.$store.state.user).then(res=>{
                this.user=res.data.rs
<<<<<<< HEAD
=======
                console.log(this.user)
>>>>>>> c75b95803d391ab0c19be27eed7e4577727d8ad0
            })
        }
    }

</script>

<style scoped>
    .MyctiList{
        background-color: #f8f8f8;
        width: 100%;
        height: 100vh;
    }
    .user {
        width: 100%;
        background-color: #ffffff;
        display: flex;;
        justify-content: flex-start;
        align-items: center;
    }

    .user img {
        width: 60px;
        height: 60px;
        margin: 2%;

    }
</style>