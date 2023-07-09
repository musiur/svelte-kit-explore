<script>
	const MenuLinks = [
		{
			text: 'About',
			link: '/about'
		},
		{
			text: 'Contact',
			link: '/contact'
		}
	];
</script>

<header>
	<nav class="container py-2 backdrop-blur bg-white/60 flex items-center justify-between gap-10">
		<a
			data-sveltekit-preload-data="tap"
			href="/"
			class="text-xl lg:text-2xl font-black hover:no-underline">TSC</a
		>
		<ul class="flex items-center justify-between gap-5">
			{#each MenuLinks as link}
				<li>
					<a data-sveltekit-preload-data="tap" href={link.link}>
						{link.text}
					</a>
				</li>
			{/each}
		</ul>
		<a data-sveltekit-preload-data="tap" href="/auth/login">
			<button class="btn">Login</button>
		</a>
	</nav>
</header>
