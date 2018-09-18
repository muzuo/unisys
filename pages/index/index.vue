<template>
	<view class="content">
		<text class="title">{{title}}</text>
		<text>{{rsg}}</text>
		<button @click="clickBtn">点击按钮</button>
	</view>
</template>

<script>
	export default {
		data: {
			title: 'Hello'
		},
		beforeCreate:function(){
			this.title='abc';
			console.log('abbc');
		},
		onLoad:function(){
			this.title='qqqqq';
			console.log('qqqwe');
		},
		computed:{
			rsg:function(){
				return 1+1;
			}
		},
		methods:{
			clickBtn:function(){
				uni.showToast({
					title:'点击按钮',
					icon:'success'
				})
			}
		}
	}
</script>

<style>
	.content {
		flex: 1;
		justify-content: center;
		align-items: center;
	}

	.title {
		font-size: 36px;
		color: #8f8f94;
	}
</style>
