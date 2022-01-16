<script>
	let value = '';
	let inputEl;
	function handleKeypress(event) {
		// if key is /
		if (event.key === '/') {
			inputEl.focus();
		}
	}
</script>

<svelte:head>
	<title>My Typing</title>
	<meta charset="UTF-8" />
	<script src="https://cdn.tailwindcss.com"></script>
	<meta name="viewport" content="initial-scale=1.0, width=device-width" />
</svelte:head>
<svelte:window on:keyup={handleKeypress} />

<div class={`h-full w-full flex-1 pt-12 bg-rose-800 flex flex-col`}>
	<div class="w-full max-w-screen-xl mx-auto sm:px-4">
		<input
			bind:this={inputEl}
			bind:value
			class="w-full px-4 py-2 rounded-md shadow-md"
			placeholder="Press / to focus"
		/>
		<h1 class="text-6xl text-purple-400 mt-12 flex-1">{value}</h1>
	</div>
</div>
