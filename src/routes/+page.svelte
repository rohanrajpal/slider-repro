<script lang="ts">
	import { Slider } from 'bits-ui';

	let value = [100];
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

Here you go

<Slider.Root
	max={1000000}
	bind:value
	class="relative flex w-full touch-none select-none items-center"
	let:thumbs
>
	<span class="bg-secondary relative h-2 w-full grow overflow-hidden rounded-full">
		<Slider.Range class="bg-primary absolute h-full" />
	</span>
	{#each thumbs as thumb}
		<Slider.Thumb
			{thumb}
			class="border-primary bg-background ring-offset-background focus-visible:ring-ring block h-5 w-5 rounded-full border-2 transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50"
		/>
	{/each}
</Slider.Root>
