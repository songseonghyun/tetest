<script>
	let firstName = 'Yoshi';
	let lastName = 'Grando';
	let beltcolor = 'black';

	$: fullname = `${firstName} ${lastName}`;
	$: {
		console.log(beltcolor);
		console.log(beltcolor);
		console.log(beltcolor);
		console.log(beltcolor);
		console.log(beltcolor);
	};
	
	const handleClick = () => {
		beltcolor = 'orange';
	};
	
	const handleInput = (e) => {
			beltcolor = e.target.value;
	};
</script>

<main>
	<p>{fullname} - {beltcolor} belt</p>
	<input type="text" bind:value={firstName}>
	<input type="text" bind:value={lastName}>
	<input type="text" bind:value={beltcolor}>
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
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>