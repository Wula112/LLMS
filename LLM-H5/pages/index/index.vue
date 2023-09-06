<template>
	<view>
	<view class="top_content">
		<view class="iconfont icon-dingwei" style="font-size: 27px; margin: 5px;">
			<text style="margin:5px ;font-size: 20px;font-weight: 500;">{{position}}</text></view>
		<u-search shape="round" placeholder="搜索疾病,症状,养生保健……"></u-search>
		<view class="iconfont icon-xiaoxi-zhihui" style="font-size: 30px;margin: 5px;"></view>
	</view>
	<view>
	<u-row
	            justify="space-between"
	            customStyle="margin:15px"
	    >
	        <u-col
			align='center'
	                span="4"
	        >
	            <view style="font-weight: 400; font-size: 30px;">专科专病</view>
	        </u-col>
	        <u-col
			align='center'
	                span="3"
	        >
	            <view style="font-weight: 300; font-size: 15px;color:#a1a1a1 ">查看更多</view>
	        </u-col>
	    </u-row>
	</view>
	<!-- <view>
		<uni-card :is-shadow="true" shadow="2px 2px 2px 2px">
			<uni-grid :column="5" :show-border="false" :square="false" @change="change">
				<uni-grid-item v-for="(item ,index) in list" :index="index" :key="index">
					<view class="grid-item-box">
					<image class="image" :src="item.url" mode="aspectFill" />
					<text class="text">{{item.text}}</text>
					</view>
					</uni-grid-item>
			</uni-grid>
		</uni-card>
	</view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				position:'南京',
				// list:[
				// 	{
				// 		url:'~@/static/waike.png'
				// 		text:'外科'
				// 	},
				// 	{
				// 		url:'~@/static/neike-.png'
				// 		text:'内科'
				// 	},
				// 	{
				// 		url:
				// 		text:'外科'
				// 	},
				// 	{
				// 		url:
				// 		text:'外科'
				// 	},
				// 	{
				// 		url:
				// 		text:'外科'
				// 	},
				// ],
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.top_content {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content:space-between;
	}

</style>
