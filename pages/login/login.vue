<template>
	<form class='loginView' @submit="login">
		<view class="oauth-image">
			<image src="../../static/companyLogo.png" mode="aspectFit"></image>
		</view>
			<view class="label-3-text">易生支付手机报件</view>
		<view class="input-view">
			<view class="label-view">
				<text class="label">账号 </text>
			</view>
			<input class="input" type="text" placeholder="请输入用户名" name="userName" />
		</view>
		<view class="input-view">
			<view class="label-view">
				<text class="label">密码</text>
			</view>
			<input class="input" :password="showPassword" placeholder="请输入密码" name="userWord" />
			<view class="uni-icon uni-icon-eye" :class="[!showPassword ? 'uni-active' : '']" @click="changePassword"></view>
		</view>
		<view class="button-view">
			<button type="default" class="login" hover-class="hover" formType="submit">登录</button>
			<button type="default" class="register" hover-class="hover" formType="reset">重置</button>
		</view>
	</form>
</template>

<script>
	export default {
		data: {
showPassword:true
		},
		methods: {
			/*表单提交登录*/
			login(e) {
				console.log(e);
				console.log(this.showPassword);
			},
			changePassword(){
				this.showPassword=!this.showPassword;
			}
		}
	}
</script>


<style>
	.label-3-text {
		color: #576B95;
		font-size: 1em;
		margin: 50px 0 50px 35%;
	}
	.oauth-image {
        width: 9em;
        height: 9em;
        border: 1px  #dddddd;
        border-radius: 100px;
        margin: auto;
        background-color: #ffffff;
    }

    .oauth-image image {
        width: 7.5em;
        height: 7.5em;
        margin: 20px;
    }
</style>
