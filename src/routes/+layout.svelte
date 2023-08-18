<script>
// @ts-nocheck

</script>

<nav>
	<img src="/MONARK-LOGO1.svg" alt="Logo">

</nav>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: sans-serif;
		overflow: hidden;
	}
	nav {
		width: 100vw;
		background-color: red;
		height: 5svh;
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
		padding: 0 20px;
		margin: auto;
	}
	nav img {
		max-width: 400px;
		max-height: max-content;
	}
</style>
<slot />
