<template>
	<view>
			<u-tabbar
				:value="currentTab"
				activeColor="#2D73F0"
				inactiveColor="#d9d9d9"
				:fixed="true"
			>
				<u-tabbar-item 
					v-for="(item,i) in tabList" 
					:key="item.name"
					:text="item.text" 
					:name="item.name"
					@click="handTab(item)"
				>
					<image class="bar_img" slot='active-icon' :src="item.selectedIconPath"></image>
					<image class="bar_img" slot='inactive-icon' :src="item.iconPath"></image>
				</u-tabbar-item>
				
			</u-tabbar>
	</view>
</template>

<script>
	export default {
			name:"TabBar",
			props: {
				currentTab: {
					type: String,
					default: 'home'
				}
			},
			data() {
				return {
					tabList: [
						{
							"pagePath": "/pages/index/index",
							"iconPath": "/static/index.png",
							"selectedIconPath": "/static/index.png",
							"text": "首页",
							"name": 'home',
						},
						{
							"pagePath": "/pages/health/health",
							"iconPath": "/static/health.png",
							"selectedIconPath": "/static/health.png",
							"text": "健康",
							"name": 'health',
						},
						{
							"pagePath": "/pages/user/user",
							"iconPath": "/static/user.png",
							"selectedIconPath": "/static/user.png",
							"text": "我的",
							"name": "user"
						}
					]
				}
			},
			methods: {
				handTab(row) {
					uni.switchTab({
						url: row.pagePath
					})
				}
			}
		}
</script>

<style>
.bar_img{
		width: 200rpx;
		height: 200rpx;
	}
</style>