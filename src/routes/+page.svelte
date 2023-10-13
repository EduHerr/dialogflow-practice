<script>
	import products from "$lib/data-source/products.json";
</script>

<svelte:head>
	<title>Products</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="container">
	<h1 class="display-4 fw-bold text-center text-white">
		Productos
	</h1>

	<div class="row">
		{#each products as producto}
			<div class="col-md-4">
				<div class="card mb-4" style="width: 18rem;">
					<img src="{producto.img}" class="card-img-top" alt="...">
					<div class="card-body">
						<h5 class="card-title">
							{producto.nombre}
						</h5>
						<p class="card-text">
							{producto.description}
						</p>
					</div>
				</div>
			</div>
		{/each}
	</div>
</div>
