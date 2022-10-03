<script>
	import Timer from './_Timer.svelte';
</script>
<svelte:head>
	<link href='https://fonts.googleapis.com/css?family=Press Start 2P' rel='stylesheet'>
</svelte:head>
<div class="hero" style="font-size: 2rem;">
	<img class="sun" src="assets/sun1.png" alt=""/>
	<img class="floor" src="assets/floor.png" alt="" />	
	<img class="build" src="assets/building1.png" alt="" />
	<img class="logo" src="assets/logo1.png" alt="" />
	<div class="container">
		<img class="ring" src="assets/ring.png" alt="" />
		<div class="centered">39</div>
	</div>
	<div class="bottom">
		<!-- <Timer /> -->
		<!-- <button class="register-button"> Register </button> -->
	</div>
</div>

<style lang="scss">
	@font-face {
		font-family: valr;
		src: url('assets/Valorant.ttf');
	}
	.sun{
		position: absolute;
		top: 65%;
		left: 27%;
		transform: translate(-50%, -50%);
		max-width: 85%;
		max-height: 140vh;
	}
	.build{
		position: absolute;
		top: 59%;
		left: 27%;
		transform: translate(-50%, -50%);
		max-width: 85%;
		max-height: 60vh;
	}
	.logo{
		position: absolute;
		top: 65%;
		left: 27%;
		transform: translate(-50%, -50%);
		max-width: 85%;
		max-height: 70vh;
	}
	.floor{
		position: fixed;
		top: 100%;
		// left: 50%;
		width: 100vw;
		transform: translate(-50%, -50%);
		max-width: 100%;
		min-height: 25%;
	}
	.container {
	position: absolute;
	top: 40%;
	left: 78%;
	transform: translate(-50%, -50%);

}
	.ring{
		max-width: 100%;
		max-height: 50vh;
		animation-name: spin;
		animation-duration: 50000ms;
		animation-iteration-count: infinite;
		animation-timing-function: linear; 
}


	.centered {
	font-family: 'Press Start 2P';
	position: absolute;
	top: 50%;
	left: 50%;
	font-size: 6vw;
	transform: translate(-50%, -50%);
	}

	@keyframes spin {
		from {
			transform:rotate(0deg);
		}
		to {
			transform:rotate(360deg);
		}
	}

	@media (min-width: 1400px) {
		.register-button {
			font-size: 2em;
			padding: 1em 3em;
		}
	}

	@media (max-width: 1100px) {
		img {
			width: 50vh;
		}
	}
	@media (max-width: 768px) {
		img {
			width: 50vh;
		}
	}
	@media (max-width: 425px) {
		img {
			width: 300px;
			top: 38%;
		}
		.bottom {
			top: 70% !important;
		}
	}
	.register-button {
		font-size: 1.9rem;
		letter-spacing: 2px;
		color: #111111;
		margin: 2vw;
		padding: 8px 25px;
		font-family: 'Metal Mania';
		background-image: url('/assets/gold-texture.jpg');
		transition: 0.25s transform ease-in-out;
		&:hover {
			transform: scale(1.1);
		}
		margin-bottom: 4px;
	}
	.hero {
		width: 100%;
		height: 100vh;
		position: relative;
		text-align: center;
		scroll-snap-align: start;
	}

	.bottom {
		width: fit-content;
		margin: 0px;
		position: absolute;
		top: 75%;
		left: 50%;
		transform: translate(-50%, 0px);
		min-width: 50%;
		max-width: 100%;
	}
</style>
