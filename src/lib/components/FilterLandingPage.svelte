<script>
	let propFor = 'buy';

	function changePropFor(param) {
		propFor = param;
	}
</script>

<div class="justify-center flex">
	<!-------------------------------------- Mobile/Tab Filters --------------------------------------------------->
	<!-------------------------------------- Mobile/Tab Filters --------------------------------------------------->
	<!-------------------------------------- Mobile/Tab Filters --------------------------------------------------->
	<form
		class="w-full mx-5 flex md:hidden flex-col p-5 bg-white relative bottom-14 max-w-5xl rounded-md drop-shadow-lg gap-4"
	>
		<div class="flex flex-row justify-between">
			<button
				on:click={() => changePropFor('buy')}
				type="button"
				class={propFor == 'buy'
					? 'main-filter-btns-selected w-full border brown-border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-3 text-center mr-3 md:mr-1'
					: 'main-filter-btns-unselected w-full border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-3 text-center mr-3 md:mr-1'}
				>BUY</button
			>
			<button
				on:click={() => changePropFor('rent')}
				type="button"
				class={propFor == 'rent'
					? 'main-filter-btns-selected w-full border brown-border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-3 text-center'
					: 'main-filter-btns-unselected w-full border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-3 text-center'}
				>RENT</button
			>
		</div>
		<select
			name=""
			id=""
			value="residential"
			class="block w-full p-3 md:p-3 text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-yellow-500 focus:border-yellow-500 mr-3"
		>
			<option value="residential" label="Residential" />
			<option value="commercial" label="Commercial" />
			<option value="off-plan" label="Off-Plan" />
		</select>
		<div class="flex flex-row items-center">
			<label
				for="default-search"
				class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Search</label
			>
			<div class="relative w-full">
				<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="23"
						height="23"
						viewBox="0 0 28 28"
						fill="none"
					>
						<path
							d="M13.6668 14.9774C15.5452 14.9774 17.0679 13.4547 17.0679 11.5763C17.0679 9.69799 15.5452 8.17529 13.6668 8.17529C11.7885 8.17529 10.2658 9.69799 10.2658 11.5763C10.2658 13.4547 11.7885 14.9774 13.6668 14.9774Z"
							stroke="#AEAEAE"
							stroke-width="2.26736"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
						<path
							d="M13.667 2.50684C11.2616 2.50684 8.95476 3.46236 7.25391 5.16321C5.55306 6.86406 4.59753 9.1709 4.59753 11.5763C4.59753 13.7212 5.05327 15.1247 6.29805 16.6778L13.667 25.1804L21.0359 16.6778C22.2807 15.1247 22.7364 13.7212 22.7364 11.5763C22.7364 9.1709 21.7809 6.86406 20.08 5.16321C18.3792 3.46236 16.0723 2.50684 13.667 2.50684V2.50684Z"
							stroke="#AEAEAE"
							stroke-width="2.26736"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
					</svg>
				</div>
				<input
					type="search"
					id="default-search"
					class="block w-full p-3 pl-12 text-gray-900 rounded-lg bg-gray-50 border border-gray-300 rounded-lg"
					placeholder="Search by Location"
					required
				/>
			</div>
		</div>
		<button
			type="submit"
			class="text-black md:bottom-1.5 gold-bg focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm md:text-lg px-3 md:px-10 py-3"
			>Search</button
		>
	</form>

	<!-------------------------------------- PC Filters --------------------------------------------------->
	<!-------------------------------------- PC Filters --------------------------------------------------->
	<!-------------------------------------- PC Filters --------------------------------------------------->
	<form
		class="hidden md:flex flex-row p-5 bg-white relative bottom-14 max-w-5xl rounded-md drop-shadow-lg"
	>
		<div class="flex flex-row max-w-sm">
			<button
				on:click={() => changePropFor('buy')}
				type="button"
				class={propFor == 'buy'
					? 'main-filter-btns-selected w-full border brown-border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-2 text-center mr-3 md:mr-2'
					: 'main-filter-btns-unselected w-full border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-2 text-center mr-3 md:mr-2'}
				>BUY</button
			>
			<button
				on:click={() => changePropFor('rent')}
				type="button"
				class={propFor == 'rent'
					? 'main-filter-btns-selected w-full border brown-border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-2 text-center mr-3 md:mr-3'
					: 'main-filter-btns-unselected w-full border focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm px-6 py-2 text-center mr-3 md:mr-3'}
				>RENT</button
			>
		</div>
		<div class="flex flex-row border border-gray-300 rounded-lg bg-gray-50 items-center">
			<select
				name=""
				id=""
				value="residential"
				class="min-w-32 block w-full p-4 md:p-3 text-gray-900 rounded-lg bg-gray-50 focus:ring-purple-500 focus:border-purple-500 mr-3"
			>
				<option value="residential" label="Residential" />
				<option value="commercial" label="Commercial" />
				<option value="off-plan" label="Off-Plan" />
			</select>
			<span class="inline-flex items-center min-h-8 w-2 bg-gray-300" />
			<label
				for="default-search"
				class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white">Search</label
			>
			<div class="relative min-w-96">
				<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="28"
						height="28"
						viewBox="0 0 28 28"
						fill="none"
					>
						<path
							d="M13.6668 14.9774C15.5452 14.9774 17.0679 13.4547 17.0679 11.5763C17.0679 9.69799 15.5452 8.17529 13.6668 8.17529C11.7885 8.17529 10.2658 9.69799 10.2658 11.5763C10.2658 13.4547 11.7885 14.9774 13.6668 14.9774Z"
							stroke="#AEAEAE"
							stroke-width="2.26736"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
						<path
							d="M13.667 2.50684C11.2616 2.50684 8.95476 3.46236 7.25391 5.16321C5.55306 6.86406 4.59753 9.1709 4.59753 11.5763C4.59753 13.7212 5.05327 15.1247 6.29805 16.6778L13.667 25.1804L21.0359 16.6778C22.2807 15.1247 22.7364 13.7212 22.7364 11.5763C22.7364 9.1709 21.7809 6.86406 20.08 5.16321C18.3792 3.46236 16.0723 2.50684 13.667 2.50684V2.50684Z"
							stroke="#AEAEAE"
							stroke-width="2.26736"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
					</svg>
				</div>
				<input
					type="search"
					id="default-search"
					class="block w-full p-4 pl-12 md:p-4 md:pl-12 text-gray-900 rounded-lg bg-gray-50"
					placeholder="Search by Location"
					required
				/>
				<button
					type="submit"
					class="text-black absolute right-1.5 bottom-1.5 md:bottom-1.5 gold-bg focus:outline-none focus:ring-purple-300 font-medium rounded-lg text-sm md:text-lg px-3 md:px-10 py-2"
					>Search</button
				>
			</div>
		</div>
	</form>

	<!-------------------------------------- PC Filters End --------------------------------------------------->
	<!-------------------------------------- PC Filters End --------------------------------------------------->
	<!-------------------------------------- PC Filters End --------------------------------------------------->
</div>

<style lang="scss">
	@import '$lib/styles/main.scss';
</style>
