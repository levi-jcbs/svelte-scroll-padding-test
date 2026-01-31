<script lang="ts">
	import { afterNavigate } from "$app/navigation";
	import "./page.css";

	afterNavigate(async (navigation) => {
		const hash = navigation.to?.url.hash;

		if (navigation.type !== "enter" && hash) {
			const anchor = document.getElementById(hash.slice(1));
			if (anchor) {
				setTimeout(() => {
					anchor.scrollIntoView({
						behavior: "instant",
						inline: "start",
						block: "start",
					});
				}, 0);
			}
		}
	});
</script>

<header>Header</header>
<div id="target">Target Element</div>
