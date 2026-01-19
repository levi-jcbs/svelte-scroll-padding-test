<script lang="ts">
	import { goto } from "$app/navigation";
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<a
	href="/test"
	onclick={(e) => {
		e.preventDefault();
		goto("/test#target");
	}}>goto() Link</a>

<a href="/test#target">Normal Link</a>
