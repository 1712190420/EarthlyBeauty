<template>
	<view>
		<cu-custom style="background-color: #fff;" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">
				<view style="font-size: 20px;">设置</view>
			</block>
		</cu-custom>
		
		<view class="size cu-form-group margin-top">
			账号与安全
		</view>
		
		<view class="cu-form-group size margin-top">
			通用
		</view>
		
		<view class="cu-form-group size">
			个人资料
		</view>
		
		<view class="cu-form-group size">
			隐私
		</view>
		
		<view class="cu-form-group size margin-top">
			意见反馈
		</view>
		
		<view class="cu-form-group size">
			关于人间烟火
		</view>
		<view class="content">
		<view class="btn-row">
			<button  @tap="bindLogout" style="color: #ffffff;background-color: #ea0b3f;border-radius: 15px;">退出登录</button>
		</view>
	</view>
		
	</view>
</template>

<script>
	import service from '../../service.js';
	import {
		mapState,
		mapMutations
	} from 'vuex'
	import mInput from '../../components/m-input.vue'
	export default {
		components: {
			mInput
		},
		data() {
			return {
			
			}
		},
		methods: {
			
			bindLogout() {
				
					uni.reLaunch({
						url: '../basic/login',
					});
			
			}
		}
	}
</script>

<style>
	.size{
		height: auto;
		font-size: 15px;
	}
	.content {
		justify-content: center;
	}
	.btn-row {
	
		display: block;
		width: 70%;
		margin: 25upx auto;

	}
</style>
