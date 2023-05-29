<script>
	// @ts-ignore
	import wasm from '../../host/Cargo.toml';

	async function loadWasm() {
		if (!import.meta.env.SSR) {
			// This code will only run in the browser
			const exports = await wasm();

			// Use functions which were exported from Rust...
			console.log({ exports });
		}
	}

	loadWasm();
</script>

Rusty Vite
