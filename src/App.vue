<template>
	<div class="flex flex-col justify-start items-center m-10">
		<header>
			<h1 class="text-4xl font-bold font-raleway">#todo</h1>
		</header>
		<nav class="flex flex-row justify-around border-b border-gray-300 pb-0 font-raleway xl:w-1/2 xl:mt-10">
			<div v-for="tab in sections" :key="tab" @click.prevent.stop="selected = tab" class="grid grid-cols-1 w-1/6 cursor-pointer">
				<span class="xl:h-10 xl:leading-10 xl:text-xl font-semibold text-center">{{ tab }}</span>
				<div class="rounded-t-md border-blue-500 h-0.5" :class="{'border-t-4': tab === selected}"></div>
			</div>
		</nav>
	</div>
</template>

<script>

export default {
	name: "App",
	components: {
	},
	data: function () {
		return {
			sections: ["All", "Active", "Completed"],
			selected: "All"
		}
	}
};
</script>

<style>
#app {
	font-family: Raleway, Avenir, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
}
</style>
