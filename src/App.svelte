<script lang="ts">
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'
  import init, { greet } from '../pkg/crust'
  async function handleClick() {
   await init();
   await greet('Vite + Svelte + Rust + WebAssembly');
  }

</script>

<main>
    <h1>Vite + WebAssembly</h1>
    <button on:click={handleClick}>Click me</button>
  </main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
