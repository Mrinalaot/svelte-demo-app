<script>
	export let name;
	let library = "React"; 
	const handleClick = () => {
		library = library === "React" ? "Svelte" : "React";
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p> I Love {library} </p>
	<button on:click={handleClick}> Switch library</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	button {
		color: orange;
		border: 1px solid black;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>