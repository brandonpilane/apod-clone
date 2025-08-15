<script lang="ts">
	// TODO: Replace with actual data
	let title: string = 'Trapezium: In the Heart of Orion';
	let date: string = '13 August 2025';
	let imageLink: string =
		'https://apod.nasa.gov/apod/image/2508/OrionTrapezium_HubbleGendler_4000.jpg';
</script>

<div
	class="relative flex h-screen w-screen flex-row items-center justify-end pe-14 pt-16 font-inter"
	id="hero-container"
>
	<div class="absolute top-[50%] left-14">
		<div class="text-5xl font-black md:max-w-[70vw]">{title}</div>
		<div class="text-2xl font-extralight">{date}</div>
	</div>
	<div
		class="relative -z-10 aspect-[11/7] h-[80vh] overflow-hidden border-none motion-safe:animate-border-morph motion-reduce:rounded-4xl"
	>
		<img src={imageLink} alt={'Image: ' + title} class="object-cover object-center saturate-110" />

		<div class="absolute inset-0 bg-gradient-to-r from-[#ffffff0c] to-transparent blur-md"></div>
	</div>

	<div
		class="absolute top-0 left-0 -z-20 h-screen w-screen overflow-hidden object-center opacity-40 blur-3xl"
	>
		<img src={imageLink} alt={'Image: ' + title} class="object-cover object-center" />
	</div>
</div>
