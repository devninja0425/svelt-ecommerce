<script>
// import 'tw-elements'
// import { browser } from '$app/environment'
import { nanoid } from 'nanoid'
// import { onMount } from 'svelte'

// onMount(async () => {
// 	if (browser) await import('tw-elements/dist/src/js/index.js')
// })
const r = nanoid()
</script>

<div id="twCarousel{r}" class="carousel slide relative" data-bs-ride="carousel">
	<div class="carousel-inner relative w-full overflow-hidden">
		<slot />
	</div>

	<button
		class="carousel-control-prev absolute top-0 bottom-0 flex items-center justify-center p-0 text-center border-0 hover:outline-none hover:no-underline focus:outline-none focus:no-underline left-0"
		type="button"
		data-bs-target="#twCarousel{r}"
		data-bs-slide="prev"
	>
		<span class="carousel-control-prev-icon inline-block bg-no-repeat" aria-hidden="true"></span>

		<span class="visually-hidden">Previous</span>
	</button>

	<button
		class="carousel-control-next absolute top-0 bottom-0 flex items-center justify-center p-0 text-center border-0 hover:outline-none hover:no-underline focus:outline-none focus:no-underline right-0"
		type="button"
		data-bs-target="#twCarousel{r}"
		data-bs-slide="next"
	>
		<span class="carousel-control-next-icon inline-block bg-no-repeat" aria-hidden="true"></span>

		<span class="visually-hidden">Next</span>
	</button>
</div>
