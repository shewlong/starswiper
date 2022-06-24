<template>
	<div class="swiper-container">
	    <div class="swiper-wrapper">
	    	<slot></slot>
	    </div>
	    <!-- 如果需要分页器 -->
	    <div class="swiper-pagination"></div>
	    
	    <!-- 如果需要导航按钮 -->
	    <div class="swiper-button-prev"></div>
	    <div class="swiper-button-next"></div>
	    
	    <!-- 如果需要滚动条 -->
	    <div class="swiper-scrollbar"></div>
	</div>
</template>

<script type="text/javascript">
	import Swiper from 'swiper';
	import 'swiper/css/swiper.css'
	export default {
		name:'swiper',
		mounted(){
			const swiper = new Swiper('.swiper-container',{
				observer:true,
				observerParents:true,
				slidesPerView:1,
				pagination:{
					el:'.swiper-pagination',
					clickable:true
				}
			})
			console.log(swiper)
		}
	}
</script>

<style type="text/css">
	.swiper-container{
		width: 100%;
		height: 300px;
	}

	.swiper-wrapper{
		width: 100%;
		height: 100%;
	}

	.swiper-slide{
		width: 100%;
		height: 100%;
		background: #f40;
	}
</style>