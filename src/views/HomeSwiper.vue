<template>
	<swiper>
		<swiper-slide v-for="i in 4">
			<div class="content" slot="swiper-slide-content">content{{i}}</div>
		</swiper-slide>
	</swiper>
</template>

<script type="text/javascript">
	import {Swiper,SwiperSlide} from '@/components/mySwiper/Swiper.js';
	export default {
		name:'HomeSwiper',
		components:{
			Swiper,SwiperSlide
		}
	}
</script>