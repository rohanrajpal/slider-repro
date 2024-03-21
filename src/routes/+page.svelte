<script lang="ts">
  import { Slider } from "bits-ui";
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

Here you go

<Slider.Root max={100}>
  <Slider.Range />
  <Slider.Thumb />
  <Slider.Input />
</Slider.Root>