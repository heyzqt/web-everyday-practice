<template>
	<view>
		<view class="banner-box">
			广告位
			<view class="uni-margin-wrap">
				<swiper class="swiper" circular="true" current="1" previous-margin="20px" next-margin="20px" :indicator-dots="indicatorDots" indicator-active-color="#faa131" :autoplay="autoplay" :interval="interval" :duration="duration">
					<swiper-item @click="handleClickSwiper('A')">
						<view class="swiper-item uni-bg-red">A</view>
					</swiper-item>
					<swiper-item @click="handleClickSwiper('B')">
						<view class="swiper-item uni-bg-green">B</view>
					</swiper-item>
					<swiper-item @click="handleClickSwiper('C')">
						<view class="swiper-item uni-bg-blue">C</view>
					</swiper-item>
				</swiper>
			</view>
		</view>
		<view class="city-box">
			<view class="city-title">城市专场</view>
			<scroll-view class="scroll-view_H scroll-box" scroll-x="true" bounces="true" @scroll="scroll" show-scrollbar="false" scroll-left="-20">
				<view id="demo1" class="scroll-view-item_H uni-bg-red">A</view>
				<view id="demo2" class="scroll-view-item_H uni-bg-green">B</view>
				<view id="demo3" class="scroll-view-item_H uni-bg-blue">C</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				indicatorDots: true,
				autoplay: false,
				interval: 2000,
				duration: 500
			}
		},
		onLoad() {

		},
		methods: {
			scroll(e) {
				console.log(e);
			},
			handleClickSwiper(id) {
				console.log('click id = ', id);
			}
		}
	}
</script>

<style>
	.banner-box {
		/* width: calc(100% - 40px); */
	}
	.uni-margin-wrap {
		/* width:690rpx; */
		width: 100%;
		/* margin:0 30rpx; */
	}
	.swiper-item {
		display: block;
		height: 300rpx;
		line-height: 300rpx;
		text-align: center;
		margin: 0 10rpx;
		/* width: 90%; */
	}
	.swiper-item-active {
		/* width: 90%; */
		background: #F823FF;
	}
	::-webkit-scrollbar {
	    width: 0;
	    height: 0;
	    color: transparent;
	}
	.scroll-box {
	  scrollbar-width: none; /* firefox */
	  -ms-overflow-style: none; /* IE 10+ */
	  overflow-x: auto;
	  overflow-y: hidden;
	}
	.city-box {
		width: 100%;
	}
	.city-title {
		padding-left: 20rpx;
	}
	.scroll-view_H { 
		width: 100%;
		white-space: nowrap;
		margin-top: 20rpx;
	}
	.scroll-view-item_H:first-child {
		margin-left: 20rpx;
	}
	.scroll-view-item_H {
		display: inline-block;
		width: 45%;
		height: 160rpx;
		line-height: 160rpx;
		text-align: center;
		font-size: 36rpx;
		margin-right: 20rpx;
		border-radius: 12rpx;
	}
	.uni-bg-red {
		background: red;
	}
	.uni-bg-green {
		background: green;
	}
	.uni-bg-blue {
		background-color: blue;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
</style>
