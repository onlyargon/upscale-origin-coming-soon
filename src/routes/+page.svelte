<script lang="ts">
	import bg from '$lib/images/bg.png';
	import clouds from '$lib/images/clouds.png';
	import not from '$lib/images/not.png';
	import text from '$lib/images/text.png';
	import logo from '$lib/images/logo.png';

	let m = { x: 0, y: 0 };

	let w: number;
	let h: number;

	$: x = (m.x / w) * 2;
	$: y = (m.y / h) * 2;

	function handleMousemove(event: any) {
		m.x = event.clientX;
		m.y = event.clientY;

		console.log(x, y);
	}
</script>

<svelte:window bind:innerWidth={w} bind:innerHeight={h} />

<main class="h-[100vh] bg-[url('{bg}')] bg-cover relative" on:mousemove={handleMousemove}>
	<img
		src={clouds}
		alt="clouds"
		class="bottom-0 overflow-hidden w-[100vw] h-[100vh] absolute z-10"
	/>
	<img
		src={text}
		alt="not"
		class="bottom-0 overflow-hidden w-[100vw] h-[100vh] absolute translate-y-[{y *
			-1}%] translate-x-[{x * -1}%]"
	/>
	<img
		src={not}
		alt="not"
		class="bottom-0 overflow-hidden h-[100vh] absolute translate-y-[{y * -1}%] translate-x-[{x *
			5}%]"
	/>
	<img src={logo} alt="not" class="bottom-0 overflow-hidden w-[100vw] h-[100vh] absolute z-20" />
</main>

<style>
</style>
