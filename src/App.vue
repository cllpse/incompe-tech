<template>
	<div id="app">
		Hello World
	</div>
</template>

<script lang="ts">
	import Vue from "vue";
	import { Component } from "vue-property-decorator";

	@Component
	export default class App extends Vue
	{
		gifs = [
			"https://media.giphy.com/media/FiJN7d4JXYioU/giphy.gif",
			"https://media.giphy.com/media/H190IMjdENEhG/giphy.gif",
			"https://media.giphy.com/media/13YIVEU6Jgx0d2/giphy.gif",
			"https://media.giphy.com/media/MJZdNd4WGnfna/giphy.gif",
			"https://media.giphy.com/media/RaPRsfdcu9G24/giphy.gif",
			"https://media.giphy.com/media/4PatqyZH60RsA/giphy.gif",
			"https://media.giphy.com/media/JeU8sPDJ6RiCI/giphy.gif"
		];

		mounted()
		{
			const url = Math.floor(Math.random() * Math.floor(this.gifs.length));

			document.body.style.backgroundImage = `url(${this.gifs[url]})`;
		}
	}
</script>

<style lang="postcss">
	
	html,
	body
	{
		width: 100%;
		height: 100%;
	}

	body
	{		
		background-size: cover;
		background-position: center center;
		background-repeat: no-repeat;
	}
	
</style>

