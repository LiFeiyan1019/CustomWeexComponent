<template>
	<div class="wrapper">
		<TopImageBottomTitle :list="list" :info="perInfo" class="button" :btnClick="cusBtnClick" :title="'传递标题'" src="https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png" :color="'red'" :fontSize="'30px'" ></TopImageBottomTitle>
	</div>
</template>

<script>
	import TopImageBottomTitle from './components/TopImageBottomTitle.vue'
	const modal = weex.requireModule('modal')
	export default {
		components: {
			TopImageBottomTitle
		},
		data() {
			return {
				logo: 'https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png',
				perInfo:{name:'黎明',age:25},
				list:['元素1','元素2'],
			
			}
		},
		methods: {
			show(message) {
				modal.toast({
					message: message,
					duration: 1
				})
			},
			cusBtnClick() {
				this.show('传递事件')
			}
		}
	}
</script>

<style scoped>
	.wrapper {
		align-items: center;
	}
	
	.button {
		margin-top: 100px;
		background-color: palegoldenrod;
		width: 400px;
		height: 400px;
	}
</style>