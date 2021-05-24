<script>
import { select_multiple_value } from "svelte/internal";


	export let name = "(insert title)";
	

	function info () {
		alert("On this page you can customize your own website")
	}
	function changeHeaderColor() {
		 header.style.color = "blue"
	}
	function changeFont() {
		header.style.fontFamily = "'Times New Roman', Times, serif"

	}
	function changeBackgroundColor() {
		document.body.style.backgroundColor = "red"
	}
</script>

<main>
	<h1 id="header">Hello {name}!</h1>
	
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
	<button on:click|once={info}>Info</button>
	
	<input type = "text" bind:value={name}>
	<button on:click={changeHeaderColor}>Change color</button>
	<button on:click={changeFont}>Change font</button>
	<button on:click={changeBackgroundColor}>Change backgroundcolor</button>
	
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
		font-family:Arial, Helvetica, sans-serif
		
	}
	button {
		color: blue;
	}
	

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>