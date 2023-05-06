<script lang="ts">
	import { onMount } from 'svelte';

	/* import { Collapse, Button, Card } from 'sveltestrap';
	let isOpen = false; */

	let Toast;
	onMount(async () => {
		// Toast = (await import('bootstrap/js/dist/toast')).default;

		// const toastDiv = <HTMLDivElement>document.getElementById('liveToast');
		// const toast = new Toast(toastDiv);
		// toast.show();
	});

	const showToast = async () => {
		Toast = (await import('bootstrap/js/dist/toast')).default;

		const toastDiv = <HTMLDivElement>document.getElementById('liveToast');
		const toast = new Toast(toastDiv);
		toast.show();
	}

</script>

<div class="container">
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

	<div class="toast-container position-fixed bottom-0 end-0 p-3">
		<div id="liveToast" class="toast" role="alert" aria-live="assertive" aria-atomic="true">
			<div class="toast-header">
				<img src="..." class="rounded me-2" alt="..." />
				<strong class="me-auto">Bootstrap</strong>
				<small>11 mins ago</small>
				<button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Close" />
			</div>
			<div class="toast-body">Hello, world! This is a toast message.</div>
		</div>
	</div>

	<div class="row g-3">
		<div class="col-12">
			<!-- <Button color="primary" on:click={() => (isOpen = !isOpen)}>Toggle Collapse</Button> -->
		</div>
		<p>
			<!-- <Collapse {isOpen}>
				<Card>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto sunt facere excepturi
					quam pariatur veritatis, molestiae aperiam laborum iusto quia itaque distinctio quisquam
					nisi quo nihil unde. Recusandae eos saepe quae harum cum similique magnam corrupti
					praesentium consequatur vero rem hic reiciendis, sapiente doloremque fugiat. Alias laborum
					pariatur praesentium tempora.
				</Card>
			</Collapse> -->
			
			<button class="btn btn-primary" on:click={showToast}>
				Show Toast
			</button>
		</p>
	</div>
</div>
