<script lang="ts">
	import bg from '$lib/images/csp_01.png';
	import grid from '$lib/images/csp_10.png';
	import comingSoonText from '$lib/images/csp_11.png';
	import nut from '$lib/images/csp_02.png';
	import logo from '$lib/images/csp_05.png';
	import text from '$lib/images/csp_12.png';
</script>

<main class="h-screen overflow-hidden bg-[url('{bg}')] bg-cover bg-no-repeat">
	<!-- write a grid with 5 cols -->
	<div class="grid grid-cols-5 h-full">
		<div />
		<!-- add grid image to the second column and on top of that add coming soon -->
		<div>
			<img src={grid} alt="grid" class="h-screen w-full scale-125" />
			<img
				src={comingSoonText}
				alt="coming soon"
				class="absolute h-96 top-1/2 transform -translate-x-[30%] hover:-translate-x-[35%] duration-300 ease-in-out -translate-y-1/2"
			/>
			<img
				src={nut}
				alt="nut"
				class="absolute h-full top-1/2 transform -translate-x-[9%] hover:-translate-x-[0%] duration-300 ease-in-out -translate-y-1/2"
			/>
		</div>

		<div />

		<!-- add logo to the top of last colum -->
		<div class="col-span-2">
			<img src={logo} alt="logo" class="p-20" />
			<img
				src={text}
				alt="content"
				class="absolute h-96 top-1/2 transform -translate-x-[20%] hover:-translate-x-[10%] duration-300 ease-in-out -translate-y-1/2"
			/>
		</div>
	</div>
</main>

<style>
</style>
