<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import sound_waves from '$lib/images/sound-waves.gif';
  	import { Parallax, ParallaxLayer, StickyLayer } from 'svelte-parallax';

  	import { Avatar, Button, Card, CarouselTransition, Blockquote, Accordion, AccordionItem } from 'flowbite-svelte'
	import { offset } from '@popperjs/core';
	
	export const images = [
  {
    id: 0,
    name: "Intuitive Interface like Twitter",
    imgurl: "https://i.ibb.co/vD1T5YS/Screenshot-2023-05-15-at-13-48-44.png",
    attribution: "seers.social",
  },
  {
    id: 1,
    name: "Prediction Markets",
    imgurl: "https://i.ibb.co/RPbF56D/Screenshot-2023-05-15-at-14-39-42.png",
    attribution: "seers.social",
  },
  {
    id: 2,
    name: "User Profiles",
    imgurl: "https://i.ibb.co/QvPBZst/Screenshot-2023-05-15-at-14-45-26.png",
    attribution: "seers.social",
  },
];
</script>

<svelte:head>
	<title>TAO - Stablecoin - Lending</title>
	<meta name="description" content="Seers: Web3 Social Network" />
</svelte:head>

<section class="w-full md:flex md:flex-row mt-14">
	<div class="flex flex-col gap-4 md:w-1/2 mt-4 p-4">
		<div class="text-4xl font-bold text-center">
			Money for a brighter future
		</div>
		<div class="text-xl p-2">
			TAO is a multi-collateral controlled-peg stable asset that puts decentralization first. 
			TAO is backed by crypto assets, including ICP, ETH and BTC. 
			It's fully on-chain and governed by the community.
		</div>
		<div class="flex justify-center">
			<a href=""><Button size="lg" style="background-color: #D61F69">Demo Coming Soon</Button></a>
		</div>
	</div>
	<div class="flex flex-col md:w-1/2 mt-4 p-4">
		<img src={sound_waves} class="w-128 h-64 rounded" alt="wave"/>
		<!-- <CarouselTransition {images} loop transitionType="fade" transitionParams="{{ duration: 500 }}"  showCaptions={false} showThumbs={false} duration="5000" slideControls={false}  showIndicators={false} /> -->
	</div>
</section>


<section class="w-full flex flex-row gap-4 md:gap-8 text-2xl justify-center mt-4 p-8">
	<Blockquote size='xl'>
		<svg aria-hidden="true" class="w-10 h-10 text-gray-400 dark:text-gray-600" viewBox="0 0 24 27" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M14.017 18L14.017 10.609C14.017 4.905 17.748 1.039 23 0L23.995 2.151C21.563 3.068 20 5.789 20 8H24V18H14.017ZM0 18V10.609C0 4.905 3.748 1.038 9 0L9.996 2.151C7.563 3.068 6 5.789 6 8H9.983L9.983 18L0 18Z" fill="currentColor"/></svg>
		"The great way is easy, yet people prefer the side paths. Be aware when things are out of balance. Stay centered within the Tao" - Lao Tzu
	</Blockquote>	
</section>

<section class="w-full flex flex-row gap-8 text-2xl justify-center mt-4 p-4">
	<div class="shadow border rounded-lg p-4">
		<div class="md:flex md:flex-row w-full">
			<div class="md:w-1/2 p-4">
				<img src="https://tai.money/_next/image?url=%2F_next%2Fstatic%2Fimage%2Fpublic%2Fimg%2Fbenefit-two.90262ab04379632ef5dac3ef6e836dfc.png&w=1080&q=75" class="rounded" />
			</div>
			<div class="md:w-1/2">
				<div class="p-4 text-lg">
					<h3 class="font-bold mb-2">Over collateralized</h3>
					TAO is an over-collateralized stablecoin, backed by high-quality crypto collateral.
				</div>
				<div class="p-4 text-lg">
					<h3 class="font-bold mb-2">Decentralization First</h3>
					TAO is DAO run from day 1. Governance will determine what collateral is added.
				</div>
				<div class="p-4 text-lg">
					<h3 class="font-bold mb-2">Pre-Agreed Upon Exit Rates</h3>
					The Anti Bank-Run stable. TAO was designed to withstand the worst of market conditions.	
				</div>
			</div>
		</div>
	</div>
</section>


<section class="w-full flex flex-row gap-8 text-2xl justify-center mt-4 p-4">
	<div class="shadow border rounded-lg p-4">
		<div class="md:flex md:flex-row w-full">
			<div class="md:w-1/2">
				<div class="p-4 text-lg">
					<h3 class="font-bold mb-2">Battle Tested</h3>
					TAO uses the proven stability mechanism of Reflexer’s RAI.
				</div>
				<div class="p-4 text-lg">
					<h3 class="font-bold mb-2">Controlled-Peg Stability</h3>
					The interest rate for TAO loans is set automagically by a PID controller.
				</div>
				<div class="p-4 text-lg">
					<h3  class="font-bold mb-2">For Everyone</h3>
					TAO is distributing ownership of the system through rewards
					to anyone minting TAO or providing TAO liquidity.		
				</div>
			</div>
			<div class="md:w-1/2 p-4">
				<img src="https://tai.money/_next/image?url=%2F_next%2Fstatic%2Fimage%2Fpublic%2Fimg%2Fbenefit-one.0f49b07f184f99faf0f58754d6aa47cd.png&w=1080&q=75" class="rounded" />
			</div>
		</div>
	</div>
</section>

<section class="w-full flex flex-col gap-8 text-2xl justify-center mt-4 p-4">
	<h3  class="font-bold mb-2">Frequently Asked Questions</h3>
					
<Accordion class="w-full">
	<AccordionItem>
	  <span slot="header" class="text-xl font-medium">What is TAO protocol?</span>
	  <p class="mb-2 text-lg">The TAO protocol offers loans to holders of ICP, ETH, and BTC.
		These loans are offered in the form of TAO, a collateral-backed, stable and liquid ICRC-2 token. 
		The TAO protocol operates as a trust-minimized set of canisters smart contracts on the Internet Computer.
		</p>
	</AccordionItem>
	<AccordionItem>
	  <span slot="header"  class="text-xl font-medium">How can I use TAO protocol?</span>
	  <p class="mb-2 text-lg">Any holder of ICP, ETH, or BTC can lock these assets as collaterals for a loan. 
		Anyone can purchase the TAO token on decentralized exchanges as a stable asset.</p>
	</AccordionItem>
	<AccordionItem>
		<span slot="header"  class="text-xl font-medium">What are the key benefits of TAO?</span>
		<p class="mb-2 text-lg">The TAO protocol is a port of RAI/DAI, one of the most proven stablecoins. 
			The TAO token will adopt the stability mechanism of RAI, avoiding excessive depegging seen in other collateralized stablecoins.
			</p><p class="mb-2 text-lg">Users can also receive rewards for using TAO, by taking out a loan in TAO or also providing TAO as liquidity. 
			Rewards are distributed in the form of LAO, the operating DAO token of the TAO protocol.
			</p>
	  </AccordionItem>
	  <AccordionItem>
		<span slot="header"  class="text-xl font-medium">Why on the Internet Computer?</span>
		<p class="mb-2 text-lg">
			Running on top of the IC allows us to optimize costs for users and provide different kinds of collaterals not found in other blockchains, with a minimal amount of trust. 
		</p>
	  </AccordionItem>
	  
  </Accordion>

</section>