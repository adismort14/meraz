<script>
	import Hero from './_Hero.svelte';
	import 'lite-youtube-embed/src/lite-yt-embed.css';
</script>

<svelte:head>
	<title>Meraz '22</title>
</svelte:head>

<div class="full">
<Hero />
<section class='glimpses'>
	<div class="title">
	<h1 style='font-weight: normal'>Meraz'22 Teaser</h1>
	</div>
	<iframe src="https://www.youtube.com/embed/W0VIHUbZ680" title="" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</section>



<section class='glimpses'>
	<div class="title">
	<h1 style='font-weight: normal'>Meraz'19 Glimpses</h1>
	</div>
	<iframe src="https://www.youtube.com/embed/fjtuMhY1KK8" title="" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</section>

<section class='glimpses'>
	<div class="title">
	<h1 style='font-weight: normal'>Meraz'18 Glimpses</h1>
	</div>
	<iframe  src="https://www.youtube.com/embed/uOQbTb4-ejs" title="" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</section>
</div>

<style lang="scss">
	.full {
		background-color: #040f47;
	}
	section {
		height: 100vh;
		// padding-top: 75px;
		scroll-snap-align: start;
		scroll-padding-top: 75px;
		margin: auto;
		display: flex;
		flex-direction: column;

		.title {
			text-align: center;
			color: transparent;
			font-family: 'Metal Mania';

			letter-spacing: 3px;

			font-size: 1.3rem;
			background-position: -5px;
			h1,
			a {
				background: -webkit-linear-gradient(gold, gold, red);
				background-clip: text;
				-webkit-background-clip: text;
				-webkit-text-fill-color: transparent;
			}
			h1 {
				font-size: 2rem;
			}

			display: flex;
			margin: 0px 30px;
			div {
				display: flex;
				flex-direction: row-reverse;
				align-items: center;
				flex-grow: 1;
			}
		}
	}	
iframe{
	margin: 1% auto ;
	width: 75vw;
	height: 80vh;
}
.glimpses{
	height: 100vh;
}

@media screen and (max-width: 900px) {
	iframe{
		height: 30vh;
		width: 90vw;
		margin-top: 5vh;
		margin-bottom: 0px;
	}
	.glimpses{
		height: 70vh ;
		padding : 0px;
	}
}
</style>
