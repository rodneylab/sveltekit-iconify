<script>
	import '@fontsource/martel';
	import '@fontsource/mate';
	import GithubIcon from '$lib/components/GithubIcon.svelte';
	import TwitterIcon from '$lib/components/TwitterIcon.svelte';
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
	:global(html) {
		background-color: var(--colour-brand);
		font-family: var(--font-body);
	}

	:global(body) {
		margin: 0;
		font-weight: var(--font-weight-normal);
	}

	:global(h1) {
		font-size: var(--font-size-6);
		font-weight: var(--font-weight-black);
	}

	:global(h2) {
		font-size: var(--font-size-5);
		font-weight: var(--font-weight-bold);
	}

	:global(h1, h2) {
		font-family: var(--font-heading);
	}

	:global(:root) {
		--colour-theme: hsl(6 71% 44%); /* international orange */
		--colour-brand: hsl(40 100% 64%); /* maximum yellow red */
		--colour-alt: hsl(200 39% 59%); /* air superiority blue */
		--colour-light: hsl(340 100% 99%); /* snow */
		--colour-dark: hsl(238 44% 16%); /* space cadet */

		--spacing-1: 0.25rem;
		--spacing-4: 1rem;
		--spacing-6: 1.5rem;
		--spacing-12: 3rem;
		--spacing-18: 4.5rem;
		--spacing-24: 6rem;
		--max-width-wrapper: 48rem;

		--font-size-root: 16px;
		--font-size-3: 1.563rem;
		--font-size-5: 2.441rem;
		--font-size-6: 3.052rem;

		--font-weight-normal: 400;
		--font-weight-bold: 700;
		--font-weight-black: 900;

		--font-heading: 'Martel';
		--font-body: 'Mate';

		/* CREDIT: https://www.joshwcomeau.com/shadow-palette/ */
		--shadow-color: 40deg 79% 44%;
		--shadow-elevation-medium: -0.8px 0.8px 1.1px hsl(var(--shadow-color) / 0.4),
			-1.9px 1.9px 2.5px -1.2px hsl(var(--shadow-color) / 0.33),
			-5.4px 5.4px 7.2px -2.5px hsl(var(--shadow-color) / 0.27),
			-14.3px 14.4px 19px -3.7px hsl(var(--shadow-color) / 0.2);
	}

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
