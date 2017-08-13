<template>
<div class="component-image-slider" tab-index="0" @keyup.right="next" @keyup.left="prev">
	<div :style="{ left: leftPosition }" class="slides">
		<picture v-for="url in images" :key="url" class="slide">
			<img :src="url" alt="">
		</picture>
	</div>
	<button v-if="canGoPrev" @click="prev" class="prev">&#10094;</button>
	<button v-if="canGoNext" @click="next" class="next">&#10095;</button>
</div>
</template>

<script>
export default {
	components: {},
	props: {
		images: Array
	},
	data() {
		return { index: 0 };
	},
	computed: {
		lenght() {
			return this.images.length;
		},
		canGoNext() {
			return this.index < this.lenght - 1;
		},
		canGoPrev() {
			return this.index > 0;
		},
		leftPosition() {
			const unit = '%';
			const left = -100 * this.index;
			return left + unit;
		}
	},
	methods: {
		prev() {
			if (!this.canGoPrev) return;
			this.index -= 1;
		},
		next() {
			if (!this.canGoNext) return;
			this.index += 1;
		}
	}
};
</script>

<style src='./image-slider.css'/>

<!--
http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/1411800820_nissangt-r_wm_carreveal_week6_forzahorizon21.jpg

http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/ChevroletCorvetteZO6_MayDLC_ForzaHorizon2_01_WM.jpg

http://res.cloudinary.com/constgen/image/upload/w_1920,h_570,c_fill/Cars/14442c5e-1063-48d9-9850-537615e0333a.jpg.jpg
 -->