<template>
	<div
		id="app"
		class="area"
	>
		<nav>
			<router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link>
		</nav>
		<router-view />

		<ul class="circle">
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
		</ul>
		<ul class="square">
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
		</ul>
	</div>
</template>

<style lang="scss">
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
	}

	nav {
		padding: 30px;

		a {
			font-weight: bold;
			color: #2c3e50;

			&.router-link-exact-active {
				color: #42b983;
			}
		}
	}

	@import url("https://fonts.googleapis.com/css?family=Exo:400,700");

	* {
		margin: 0px;
		padding: 0px;
	}

	body {
		font-family: "Exo", sans-serif;
	}

	.context {
		width: 100%;
		position: absolute;
		top: 50vh;
	}

	.context h1 {
		text-align: center;
		color: #fff;
		font-size: 50px;
	}

	.area {
		background: #4e54c8;
		background: -webkit-linear-gradient(to left, #8f94fb, #4e54c8);
		width: 100%;
		height: 100vh;
	}

	// .triangle{
	//   border-right: 50px solid transparent;
	//   border-bottom: 86.6025px solid #b2ce54;
	//   border-left: 50px solid transparent;
	// }
	// 	.triangle {
	// 		position: absolute;
	// 		top: 0;
	// 		left: 0;
	// 		width: 100%;
	// 		height: 100%;
	// 		overflow: hidden;
	// 		li {
	// 			position: absolute;
	// 			display: block;
	// 			list-style: none;
	// 			width: 20px;
	// 			height: 20px;
	// 			background: rgba(255, 255, 255, 0.2);
	// 			animation: animate 25s linear infinite;
	// 			bottom: -150px;
	// 			&:nth-child(1) {
	// 				left: 25%;
	// 				width: 80px;
	// 				height: 80px;
	// 				animation-delay: 0s;
	// 			}
	// 			&:nth-child(2) {
	// 				left: 10%;
	// 				width: 20px;
	// 				height: 20px;
	// 				animation-delay: 2s;
	// 				animation-duration: 12s;
	// 			}

	// 			&:nth-child(3) {
	// 				left: 70%;
	// 				width: 20px;
	// 				height: 20px;
	// 				animation-delay: 4s;
	// 			}

	// 			&:nth-child(4) {
	// 				left: 40%;
	// 				width: 60px;
	// 				height: 60px;
	// 				animation-delay: 0s;
	// 				animation-duration: 18s;
	// 			}

	// 			&:nth-child(5) {
	// 				left: 65%;
	// 				width: 20px;
	// 				height: 20px;
	// 				animation-delay: 0s;
	// 			}

	// 			&:nth-child(6) {
	// 				left: 75%;
	// 				width: 110px;
	// 				height: 110px;
	// 				animation-delay: 3s;
	// 			}

	// 			&:nth-child(7) {
	// 				left: 35%;
	// 				width: 150px;
	// 				height: 150px;
	// 				animation-delay: 7s;
	// 			}

	// 			&:nth-child(8) {
	// 				left: 50%;
	// 				width: 25px;
	// 				height: 25px;
	// 				animation-delay: 15s;
	// 				animation-duration: 45s;
	// 			}

	// 			&:nth-child(9) {
	// 				left: 20%;
	// 				width: 15px;
	// 				height: 15px;
	// 				animation-delay: 2s;
	// 				animation-duration: 35s;
	// 			}

	// 			&:nth-child(10) {
	// 				left: 85%;
	// 				width: 150px;
	// 				height: 150px;
	// 				animation-delay: 0s;
	// 				animation-duration: 11s;
	// 			}
	// 		}
	// 	}

	.circle {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		overflow: hidden;
		pointer-events: none;
		li {
			position: absolute;
			display: block;
			list-style: none;
			width: 20px;
			height: 20px;
			background: rgba(255, 255, 255, 0.2);
			animation: circle_animate 25s linear infinite;
			bottom: -150px;
			&:nth-child(1) {
				left: 25%;
				width: 80px;
				height: 80px;
				animation-delay: 0s;
			}
			&:nth-child(2) {
				left: 10%;
				width: 20px;
				height: 20px;
				animation-delay: 2s;
				animation-duration: 12s;
			}

			&:nth-child(3) {
				left: 70%;
				width: 20px;
				height: 20px;
				animation-delay: 4s;
			}

			&:nth-child(4) {
				left: 40%;
				width: 60px;
				height: 60px;
				animation-delay: 0s;
				animation-duration: 18s;
			}

			&:nth-child(5) {
				left: 65%;
				width: 20px;
				height: 20px;
				animation-delay: 0s;
			}
		}
	}
	.square {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		overflow: hidden;
		pointer-events: none;

		li {
			position: absolute;
			display: block;
			list-style: none;
			width: 20px;
			height: 20px;
			background: rgba(255, 255, 255, 0.2);
			animation: square_animate 25s linear infinite;
			bottom: -150px;

			&:nth-child(1) {
				left: 75%;
				width: 110px;
				height: 110px;
				animation-delay: 3s;
			}

			&:nth-child(2) {
				left: 15%;
				width: 150px;
				height: 150px;
				animation-delay: 7s;
			}

			&:nth-child(3) {
				left: 50%;
				width: 25px;
				height: 25px;
				animation-delay: 15s;
				animation-duration: 45s;
			}

			&:nth-child(4) {
				left: 20%;
				width: 15px;
				height: 15px;
				animation-delay: 2s;
				animation-duration: 35s;
			}

			&:nth-child(5) {
				left: 85%;
				width: 150px;
				height: 150px;
				animation-delay: 0s;
				animation-duration: 11s;
			}
		}
	}

	@keyframes square_animate {
		0% {
			transform: translateY(0) rotate(0deg);
			opacity: 1;
			border-radius: 0;
		}

		100% {
			transform: translateY(-1000px) rotate(720deg);
			opacity: 0.3;
			border-radius: 50%;
		}
	}
	@keyframes circle_animate {
		0% {
			transform: translateY(0) rotate(0deg);
			opacity: 1;
			border-radius: 100%;
		}

		100% {
			transform: translateY(-1000px) rotate(720deg);
			opacity: 0.3;
			border-radius: 100%;
		}
	}
</style>
