<template>
	<div id="app">
		<div class="grid">
			<div class="grid__head">
				<div class="logo"><img src="./assets/img/logo.png" width="100%" alt=""></div>
			</div>
			<div class="grid__body">
				<div class="header">
					<span class="font-lt-72">международный</span>
					<h1 class="font-eb-100">нутра-митап 2019</h1>
				</div>

				<div class="subheader"><span class="font-eb-36">для топовых вебмастеров и сервисов</span></div>

				<div class="graffiti">
					<img src="./assets/img/beach-party.svg" height="100%" alt="" class="md">
					<img src="./assets/img/beach-party2.svg" height="100%" alt="" class="sm">
				</div>

				<div class="info">
					<div class="info__card">
						<div class="date">
							<span>киев</span>
							<span class="separare-left">25 июля</span>
						</div>

						<div class="svg-holder"><img src="./assets/img/city-beach-club.svg" height="100%" alt=""></div>
					</div>

					<div class="info__card info__card_details">
						<div class="soon"><span>подробности <br>скоро..</span></div>

						<div class="socials-list">
							<a href="#" class="socials-list__item"><img src="./assets/img/email-logo.svg" width="100%" alt=""></a>
							<a href="#" class="socials-list__item"><img src="./assets/img/facebook-logo.svg" width="100%" alt=""></a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'app'
	}
</script>

<style lang="scss">
html {
	font-size: 18px;
}

body {
	width: 100%;
	height: 100%;
	margin: 0;
	padding: 0;
	font-family: 'Montserrat', sans-serif;
	color: #222;
}

h1, h2, h3 {
	margin: 0;
	line-height: 1.1;
}

.grid {
	width: 100%;
	height: 100vh;

	&__head {
		display: flex;
		height: 180px;

		.logo {
			width: 300px;
			margin: auto;
		}
	}

	&__body {
		height: calc(100vh - 180px);
		padding: 53px 75px 75px;
		box-sizing: border-box;
		background-image: url(./assets/img/bg.jpg);
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
		color: #fff;
	}
}

.header {
	text-align: center;
	letter-spacing: 4.09px;
	text-transform: uppercase;
}

.subheader {
	width: 100%;
	max-width: 63.8rem;
	margin: 15px auto 25px;
	padding: 8px 0;
	box-sizing: border-box;
	text-align: center;
	text-transform: uppercase;
	letter-spacing: 2px;
	color: #895411;
	border-radius: 5px;
	background-color: #fff;
}

.graffiti {
	height: 130px;
	text-align: center;
	margin: 0 auto;
	
	.sm {
		display: none;
	}
}

.info {
	display: flex;
	justify-content: center;
	margin-top: 56px;

	&__card {
		position: relative;
		box-sizing: border-box;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		width: 100%;
		max-width: 870px;
		padding: 58px 0;
		background: rgba(81, 37, 0, 0.5);
		border-radius: 5px;
		z-index: 2;

		&:not(:last-child) {
			margin-right: 29px;
		}

		.svg-holder {
			height: 74px;
			margin-top: 24px;
		}
	}
}

.date {
	text-align: center;
	text-transform: uppercase;
	letter-spacing: 3.41px;
	font-weight: 800;
	font-size: 3.333rem;

	.separare-left {
		position: relative;
		margin-left: 48px;

		&:before {
			content: '';
			position: absolute;
			left: -24px;
			top: 50%;
			margin-top: -18px;
			height: 42px;
			width: 3px;
			background-color: #fff;
		}
	}
}

.soon {
	margin-right: 95px;
	text-align: left;
	text-transform: uppercase;
	letter-spacing: 1.5px;
	font-weight: 300;
	font-size: 2.222rem;
}

.socials-list {
	display: flex;
	flex-wrap: wrap;
	justify-content: flex-start;

	&__item {
		width: 70px;

		&:not(:last-child) {
			margin-right: 42px;
		}
	}
}

.font-lt-72 {
	font-weight: 300;
	font-size: 4rem;
}

.font-eb-100 {
	font-weight: 800;
	font-size: 5.555rem;
}

.font-eb-36 {
	font-weight: 800;
	font-size: 2rem;
}

@media screen and (max-width: 1700px) {
	.soon {
		margin-right: 30px;
	}
}

@media screen and (max-width: 1440px) {
	html {
		font-size: 12px;
	}

	.grid__body {
		display: flex;
		flex-wrap: wrap;
		flex-direction: column;
		justify-content: center;
	}
	
	.graffiti {
		height: 100px;
	}

	.socials-list__item:not(:last-child) {
		margin-right: 20px;
	}
}

@media screen and (max-width: 1200px) {
	.grid__body {
		padding: 25px;
	}
}

@media screen and (max-width: 1050px) {
	.info__card_details {
		flex-direction: column;
	}

	.soon {
		margin-right: 0;
		margin-bottom: 16px;
		text-align: center;
	}
}

@media screen and (max-width: 991px) {
	html {
		font-size: 10px;
	}

	.grid__head {
		height: 150px;

		.logo {
			width: 276px;
		}
	}

	.grid__body {
		height: calc(100vh - 150px);
		padding: 25px 15px;
	}

	.info {
		width: 100%;
		flex-direction: column;
		align-items: center;

		&__card {
			flex-direction: column;
			padding: 40px 10px;
			
			&:not(:last-child) {
				margin-right: 0;
				margin-bottom: 20px;
			}

			.svg-holder {
				height: 60px;
			}
		}
	}
	
	.date .separare-left {
		margin-left: 36px;

		&:before {
			left: -18px;
		}
	}
}

@media screen and (max-width: 768px) {
	.grid__head {
		height: 100px;

		.logo {
			width: 185px;
		}
	}

	.grid__body {
		height: auto;
		min-height: calc(100vh - 100px);
	}

	.subheader {
		padding: 8px 20px;
	}

	.font-lt-72 {
		font-size: 30px;
		letter-spacing: 1.37px;
	}
	
	.font-eb-100 {
		font-size: 30px;
		letter-spacing: 1.51px;
	}

	.graffiti {
		width: 100%;
		max-width: 300px;
		height: auto;

		img {
			height: auto;
			width: 100%;
		}

		.md {
			display: none;
		}

		.sm {
			display: block;
		}
	}

	.date {
		span {
			display: block;
		}

		.separare-left {
			margin-left: 0;

			&:before {
				display: none;
			}
		}
	}

	.socials-list__item {
		width: 45px;
	}
}

@media screen and (max-width: 400px) {
	.font-lt-72 {
		font-size: 24px;
		letter-spacing: 1.37px;
	}
	
	.font-eb-100 {
		font-size: 24px;
		letter-spacing: 1.51px;
	}

	.svg-holder {
		width: 100%;

		img {
			height: auto;
			width: 100%;
		}
	}
}

@media screen and (max-height: 1080px) {
	.grid__body {
		height: auto;
	}
}
</style>
