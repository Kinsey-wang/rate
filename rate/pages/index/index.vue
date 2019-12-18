<template>
	<view class="rate-content">
			<uniRate text="1" size="34" margin="10" :value="rateValue" @change="rateChange"></uniRate>
			<view class="rate-tips">{{rateTitleArr[rateValue-1]}}</view>
	</view>
</template>

<script>
	import uniRate from '@/components/rate/uni-rate.vue'
	export default {
		components:{uniRate},
		data() {
			return {
				rateValue:1,
				rateTitleArr:['很差','差','中','好','很好']
			}
		},
		methods: {
			rateChange(val){
			  this.rateValue=val.value
			}
		}
	}
</script>

<style lang="scss">
	.rate-content{
		margin-top: 60rpx;
		flex-direction: column;
		display: flex;
		align-items: center;
		justify-content: center;
		.rate-tips{
			margin-top: 10rpx;
			font-size: 32rpx;
		}
	}
</style>
