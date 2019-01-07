<template>
    <div class="page">
        <div class="loginwarrp">
            <div class="logo">管理员登陆</div>
            <div class="login_form">
                <form ref="formLogin" :model="formLogin" :rules="ruleLogin">
                    <li class="login-item">
                            <span>用户名：</span>
                            <input v-model="formLogin.username" type="text" class="login_input">
                            <span id="count-msg" class="error"></span>
                    </li>
                    <li class="login-item">
                        <span>密  码：</span>
                        <input v-model="formLogin.password" type="password" class="login_input">
                        <span id="password-msg" class="error"></span>
                    </li>
                    <li class="login-sub">
                        <input type="button" @click="" value="登录"/><span style="padding: 20px"></span>
                        <input type="reset" name="Reset" value="重置"/>
                    </li>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "login",
        data() {
            return {
                code: null,
                formLogin: {
                    username: 'zhouchong',
                    password: '123456'
                },
                ruleLogin: {
                    username: [
                        {required: true, message: 'please fill in your name', trigger: 'blur'}
                    ],
                    password: [
                        {required: true, message: 'please fill in your password', trigger: 'blur'}
                    ]
                }
            }
        },
        methods:{
            login(formLgoin){
                this.$refs[formLgoin]
            }
        }
    }
</script>

<style scoped>
    .loginwarrp {
        margin: 250px auto;
        width: 400px;
        padding: 30px 50px;
        background: #FFFFFF;
        overflow: hidden;
        font-size: 14px;
        font-family: '微软雅黑', '文泉驿正黑', '黑体';
    }

    .loginwarrp .logo {
        width: 100%;
        height: 44px;
        line-height: 44px;
        font-size: 20px;
        text-align: center;
        border-bottom: 1px solid #ddd;
    }

    .loginwarrp .login_form {
        margin-top: 15px;
    }

    .loginwarrp .login_form .login-item {
        padding: 2px 8px;
        border: 1px solid #dedede;
        border-radius: 8px;
        margin-top: 10px;
    }

    .loginwarrp .login_form .login_input {
        height: 35px;
        border: none;
        line-height: 35px;
        width: 200px;
        font-size: 14px;
        outline: none;
    }

    .loginwarrp .login_form .verify {
        float: left;
    }

    .loginwarrp .verify .verify_input {
        width: 160px;
    }

    .loginwarrp .verifyimg {
        height: 30px;
        margin: 20px 0 0 20px;
    }

    .loginwarrp .login-sub {
        text-align: center;
    }

    .loginwarrp .login-sub input {
        margin-top: 15px;
        background: #45B549;
        line-height: 35px;
        width: 150px;
        color: #FFFFFF;
        font-size: 16px;
        font-family: '微软雅黑', '文泉驿正黑', '黑体';
        border: none;
        border-radius: 5px;
    }

    .loginwarrp .login_form .login-item .error {
        color: #F00;
        font-family: '微软雅黑', '文泉驿正黑', '黑体';
    }
</style>
