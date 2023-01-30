<script lang="ts">
	import { Collapse, Button, Card } from 'sveltestrap';
	let isOpen = false;
</script>

<div class="container">
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

	<div class="row g-3">
		<div class="col-12">
			<Button color="primary" on:click={() => (isOpen = !isOpen)}>Toggle Collapse</Button>
		</div>
		<p>
			<Collapse {isOpen}>
				<Card>
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto sunt facere excepturi
					quam pariatur veritatis, molestiae aperiam laborum iusto quia itaque distinctio quisquam
					nisi quo nihil unde. Recusandae eos saepe quae harum cum similique magnam corrupti
					praesentium consequatur vero rem hic reiciendis, sapiente doloremque fugiat. Alias laborum
					pariatur praesentium tempora.
				</Card>
			</Collapse>
		</p>
	</div>
</div>
