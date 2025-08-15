<script lang="ts">
	import { onMount } from 'svelte';
	let width: number = 0;

	const updateWidth = () => {
		width = window.innerWidth;
	};

	onMount(() => {
		updateWidth();
		window.addEventListener('resize', updateWidth);
		return () => {
			window.removeEventListener('resize', updateWidth);
		};
	});
</script>

<nav
	class="absolute top-0 right-0 left-0 flex w-screen flex-row items-center justify-between px-14 py-4 font-inter"
>
	<a
		class="cursor-pointer text-2xl font-bold"
		href="/"
		aria-label="Astronomy Picture of the Day Home">APOD.</a
	>
	<p class="max-w-[60vw] text-right align-middle">
		{#if width < 768}
			Discover the cosmos!
		{:else if width < 1536}
			Discover the cosmos! Each day brings a unique image of our universe with a brief astronomer’s
			note.
		{:else}
			From breathtaking nebulae to distant galaxies, each day's image comes with a brief
			astronomer's note.
		{/if}
	</p>
</nav>
