<script>
	import GithubIcon from '$lib/components/GithubIcon.svelte';
	import TwitterIcon from '$lib/components/TwitterIcon.svelte';
	import '$lib/styles/global.css';
	import '@fontsource/martel';
	import '@fontsource/mate';
</script>

<svelte:head>
	<title>My Blog</title>
	<meta name="description" content="My blog all about me" />
</svelte:head>

<header class="header-container"><h1>My Blog</h1></header>
<main class="main-container">
	<div class="main-content">
		<h2>About me</h2>
		<p>I&rsquo;m Nemo, a developer from New City, My Land.</p>
		<p>I build fast sites in SvelteKit!</p>
		<p>Twitter and GitHub links in footer 👇🏽</p>
	</div>
</main>
<footer class="footer-container">
	<nav class="links">
		<a aria-label="Open my Git Hub page" href="https://github.com"
			><span class="icon"><GithubIcon /></span></a
		>
		<a aria-label="Open my Twitter profile" href="https://twitter.com"
			><span class="icon"><TwitterIcon /></span></a
		>
	</nav>
</footer>

<style>
	.header-container {
		display: grid;
		background-color: var(--colour-dark);
		color: var(--colour-light);
		height: var(--spacing-24);
		place-content: center;
	}

	.main-container {
		background-color: var(--colour-theme);

		/* CREDIT: https://www.joshwcomeau.com/gradient-generator/ */
		background-image: linear-gradient(
			45deg,
			hsl(6deg 71% 44%) 0%,
			hsl(6deg 71% 45%) 14%,
			hsl(6deg 70% 46%) 29%,
			hsl(6deg 71% 47%) 43%,
			hsl(6deg 71% 49%) 57%,
			hsl(6deg 71% 50%) 71%,
			hsl(6deg 71% 51%) 86%,
			hsl(6deg 71% 52%) 100%
		);

		box-shadow: var(--shadow-elevation-medium);
		border-radius: var(--spacing-1);
		color: var(--colour-light);
		width: min(100% - var(--spacing-12), var(--max-width-wrapper));
		margin: var(--spacing-18) auto;
		min-height: calc(100vh - var(--spacing-24) - var(--spacing-18) - var(--spacing-18));
		font-size: var(--font-size-3);
	}

	.main-content {
		display: flex;
		flex-direction: column;
		padding: var(--spacing-6) var(--spacing-12);
	}
	.footer-container {
		display: grid;
		background-color: var(--colour-light);
		color: var(--colour-alt);
		place-content: center;
	}
	.footer-container a {
		color: var(--colour-alt);
	}
	.footer-container a:focus,
	.footer-container a:hover {
		color: var(--colour-dark);
	}

	.links {
		padding: var(--spacing-18);
	}
	.icon {
		margin: var(--spacing-4);
	}
</style>
