<script>
import ImageSlider from './components/image-slider/image-slider.vue';

export default {
	components: {
		ImageSlider
	},
	data() {
		return {
			images: [
				'http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1411800820_nissangt-r_wm_carreveal_week6_forzahorizon21.jpg',

				'http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/ChevroletCorvetteZO6_MayDLC_ForzaHorizon2_01_WM.jpg',

				'http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/14442c5e-1063-48d9-9850-537615e0333a.jpg.jpg',

				'http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1409758275_2012-jaguar-xkr-s.jpg',

				'http://www.insidegames.ch/wp-content/gallery/forza-horizon-3/forza-horizon-3-gamescom-2016-screenshot-03.jpg'
			]
		};
	}
};
</script>
<style>
html,body {
	width: 100%;
	height: 100%;
	margin: 0;
	padding: 0;
}

body {
	box-sizing: border-box;
	padding: 20px;
}

.image-slider {
	height: 300px;
}
</style>

<template>
  <body>
    Application started
	<image-slider class="image-slider" :images="images"/>
	<image-slider class="image-slider" :images="images"/>
  </body>
</template>