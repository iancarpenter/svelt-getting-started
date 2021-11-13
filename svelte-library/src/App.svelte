<script>
	import { Route, Router } from "svelte-routing";
	import Detail from "./detail/Detail.svelte";
	import Library from "./Library/Library.svelte";

	export let url = "";
</script>
<style>
	main {
		passing: var(--spacingLarge);
	}
</style>
<Router {url}>
<main>
	<Route path="/books/:id" let:params>
		<Detail id={params.id}/>
	</Route>
	<Route path="/">
		<Library />
	</Route>
</main>
</Router>


