<script>
	import { onMount } from 'svelte';

	onMount(() => {
		document.addEventListener('scroll', () => {
			const navbar = document.getElementById('navbar');
			const whatsappBtn = document.getElementById('whatsapp-btn');
			const mobileMenuBtn = document.getElementById('mobile-menu-btn');
			const logoImg = document.getElementById('logo-img');
			const navbarBtns = document.getElementsByName('navbar-text');

			if (window.scrollY > 0) {
				navbar.classList.remove('bg-transparent');
				navbar.classList.add('bg-white');
				//
				whatsappBtn.classList.remove('text-white');
				whatsappBtn.classList.add('text-green-700');
				//
				mobileMenuBtn.classList.remove('text-white');
				mobileMenuBtn.classList.add('text-black');
				//
				logoImg.src = '/images/logo/logo.png';
				//
				for (let index = 0; index < navbarBtns.length; index++) {
					navbarBtns[index].classList.add('text-black');
					navbarBtns[index].classList.remove('text-white');
				}
			} else {
				navbar.classList.remove('bg-white');
				navbar.classList.add('bg-transparent');
				//
				whatsappBtn.classList.remove('text-green-700');
				whatsappBtn.classList.add('text-white');
				//
				mobileMenuBtn.classList.remove('text-black');
				mobileMenuBtn.classList.add('text-white');
				//
				logoImg.src = '/images/logo/logo-white.png';
				//
				for (let index = 0; index < navbarBtns.length; index++) {
					navbarBtns[index].classList.add('text-white');
					navbarBtns[index].classList.remove('text-black');
				}
			}
		});
	});
</script>

<header>
	<nav id="navbar" class="bg-transparent py-3 fixed w-full z-20 top-0 left-0">
		<div class="max-w-screen-2xl flex flex-wrap items-center justify-between mx-auto p-4">
			<a href="/" class="flex items-center">
				<img id="logo-img" src="/images/logo/logo-white.png" class="h-full" width="150" height="200" alt="A House" />
			</a>
			<div class="flex md:order-2">
				<button
					id="mobile-menu-btn"
					data-collapse-toggle="navbar-sticky"
					type="button"
					class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-white focus:text-black rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200"
					aria-controls="navbar-sticky"
					aria-expanded="false"
				>
					<span class="sr-only">Open main menu</span>
					<svg
						class="w-5 h-5"
						aria-hidden="true"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 17 14"
					>
						<path
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M1 1h15M1 7h15M1 13h15"
						/>
					</svg>
				</button>
			</div>
			<div
				class="items-center justify-between hidden w-full md:flex md:w-auto md:order-2"
				id="navbar-sticky"
			>
				<ul
					class="items-center flex flex-col p-4 md:p-0 mt-4 font-medium border border-gray-100 rounded-lg md:flex-row md:space-x-8 md:mt-0 md:border-0"
				>
					<li>
						<a
							name="navbar-text"
							href="/"
							class="text-white block py-2 pl-3 pr-4 bg-purple-700 rounded md:bg-transparent gold-text md:p-0"
							aria-current="page">Home</a
						>
					</li>
					<li>
						<a
							name="navbar-text"
							href="#property"
							class="text-white block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent hover-gold-text md:p-0"
							>About Us</a
						>
					</li>
					<li>
						<a
							name="navbar-text"
							class="text-white block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent hover-gold-text md:p-0"
							>Explore Properties</a
						>
					</li>
					<li>
						<a
							name="navbar-text"
							href="#service"
							class="text-white block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent hover-gold-text md:p-0"
							>Assist Me</a
						>
					</li>
					<li>
						<button
							id="whatsapp-btn"
							type="button"
							class="text-white bg-white-700 border-solid border-2 hover:border-green-600 focus:ring-4 focus:outline-none focus:ring-purple-300 font-medium rounded-lg md:text-lg px-4 py-2 text-center mr-3 md:mr-0"
						>
							<div class="flex flex-row items-center">
								<img
									class="drop-shadow-md"
									src="/images/whatsapp.png"
									width="20"
									height="10"
									alt="whatsapp"
								/>
								<span class="pl-2">Whatsapp</span>
							</div>
						</button>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</header>

<style lang="scss">
	@import '$lib/styles/main.scss';
</style>
