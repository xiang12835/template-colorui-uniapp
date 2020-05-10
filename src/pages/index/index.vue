<template>
	<view>
		<cu-custom bgColor="bg-gradual-blue" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">导航栏</block>
		</cu-custom>
		<view class="content">
			{{title}}
		</view>
	</view>
</template>
<script>
	import { test200 } from "@/apis/test.js"
	export default {
	    data() {
	        return {
	            title: ''
	        }
	    },
	    onLoad() {
	        this.test()
	    },
	    methods: {
	        // 测试获取数据
	        test () {
	            test200().then(res => {
	                this.title = res.data
	            })
	        }
	    }
	}
</script>

<style>

</style>
