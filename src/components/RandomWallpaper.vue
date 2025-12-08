<template>
	<div class="randomWallpaper">
		<img :src="randomWallpaper" alt="Random Wallpaper" />
	</div>
</template>

<script>
export default {
	data() {
		return {
			wallpapers: [
				'wallpapers/wallpaper-1.webp',
				'wallpapers/wallpaper-2.jpg',
				'wallpapers/wallpaper-3.jpg',
				'wallpapers/ernst-1.jpg',
				'wallpapers/ernst-2.jpg',
				'wallpapers/ernst-3.jpg',
				'wallpapers/ernst-4.jpg',
				'wallpapers/ernst-5.jpg',
          'wallpapers/kerguelen.jpg',
          'wallpapers/monet-magpie.jpg',
          'wallpapers/np-snow.jpg'
			]
		};
	},
	computed: {
		randomWallpaper() {
			const randomIndex = Math.floor(Math.random() * this.wallpapers.length);
			return this.wallpapers[randomIndex];
		}
	}
};
</script>

<style scoped>
.randomWallpaper {
	width: 400px;
	height: 300px;
	overflow: hidden;
	border-radius: 10px;
	margin: 10px;
	object-fit: cover;
	background: rgba(16, 21, 61, 0.5);
	backdrop-filter: blur(10px);
	-webkit-backdrop-filter: blur(10px);
	border-radius: 15px;
	box-shadow: 0 0.5px 0 1px rgba(255, 255, 255, 0.13) inset, 0 1px 0 0 rgba(255, 255, 255, 0.1) inset, 0 4px 16px rgba(0, 0, 0, 0.2);
}

img{
	width: 400px;
	height: 300px;
	object-fit: cover;
	object-position: center center;
	opacity: .9;
}
</style>
