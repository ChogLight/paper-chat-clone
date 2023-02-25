<script>
// @ts-nocheck

	import './app.css';
	import Navbar from '../components/Navbar.svelte';
	let dark = true
	let darkMode
	const checkDark = (dark) => {
		return dark?
			"dark":
			""
	}
	$:darkMode = checkDark(dark)
</script>

<div class="bg-[#050f64] dark:bg-slate-900 text-white text-sm font-mono flex-col h-screen duration-1000 {darkMode}">

	<Navbar bind:dark darkMode = {darkMode}/>
	<div>
		<main class="basis-4/5 bg-white dark:bg-slate-700 {darkMode}">
			<slot />
		</main>
	</div>
</div>

