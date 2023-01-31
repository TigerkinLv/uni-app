<template>
	<view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
			<swiper-item v-for="(item,index) in list" :key="index">
				<navigator class="swiper-item" :url="'/subpkg/goods/goods?goodsId='+item">
					{{item}}
				</navigator>
			</swiper-item>
		
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[1,2,3]
			};
		},
		mounted() {
			uni.$showMsg();

		}
	}
</script>

<style lang="scss">

</style>
