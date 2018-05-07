<template>
	<div class="wrap" @click="btnClick">
		<!--图片-->
		<image class="image" resize="contain" :src="src"></image>
		<!--文本-->
		<text class="name" :style="{color:color,fontSize:fontSize}">{{title}}</text>
		<!--对象-->
		<text class="object">{{info.name}} {{info.age}}</text>
		<!--数组-->
		<text v-for="item in list">{{item}}</text>

	</div>
</template>

<script>
	export default {
		props: [ 'src','color', 'fontSize', 'title', 'btnClick','info','list'],
		data(){
			return{
				
			}
		}
	}
</script>

<style scoped>
	.wrap {
		/*background-color: pink;*/
		justify-content: center;
		align-items: center;
	}
	
	.image {
		background-color: blue;
		width: 90px;
		height: 90px;
		/*border-radius: 60px;*/
	}
	
	.name {
		/*background-color: aquamarine;*/
		margin-top: 10px;
		/*font-size: 22px;
		color: #222222;*/
	}
	.object{
		color: green;
		font-size: 28px;
	}
</style>