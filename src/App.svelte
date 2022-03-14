<script>
	let name = 'Nested Components, HTML tags, and $:'
	import Nested from "./Nested.svelte";
	let urlString = "This is a boom example with a <strong>HTML</strong> " +
			"and a hyperlink redirect to <a href='https://google.ca'>Google</a>";
</script>

<main>
	<h1><b>Example for {name}!</b></h1>
	<p>{@html urlString}</p>
	<Nested count = {10}/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		background-color: -moz-mac-accentregularshadow;
	}

	h1 {
		color: rgb(166,137,124);
		font-family: "Times New Roman",cursive;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 100;
	}

	p{
		color: rgb(219,207,202);
		font-size: 25px;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>