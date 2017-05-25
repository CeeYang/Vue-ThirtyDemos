<template>
	<div class="welcome" :class="{hiden:hiden}">
		<img src="https://sinacloud.net/vue-wechat/images/welcome.jpg" alt="">
	</div>
</template>

<script>
	export default {
		data () {
			return {
				hiden:false
			}
		},
		mounted () {

			setTimeout(() => {
				this.hiden = true
			}, 1000)
			
		}
	}
</script>

<style>
	.welcome {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: #000b17;
		animation: welcome 0.5s;
		transition: 0.3;
	}

	.welcome img {
		width: 100%;
	}

	.welcome.hiden {
		opacity: 0;
    	visibility: hidden;
	}
</style>