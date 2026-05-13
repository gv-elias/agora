<script lang="ts">
  import "./layout.css";
  import logo from "$lib/assets/logo.svg";

  let { children } = $props();
</script>

<svelte:head>
  <title>Ágora</title>
  <link rel="icon" href={logo} />
</svelte:head>


<div class="flex h-screen bg-stone-50 text-stone-800 font-sans">
  
  <aside class="w-64 bg-stone-100 border-r border-stone-200 flex flex-col p-6 shadow-sm z-10">
    
    <div class="flex items-center gap-3 mb-10 mt-2">
        <img src={logo} alt="Logo de Ágora" class="w-10 h-10 transition-transform hover:scale-105" />
        <span class="text-2xl font-bold tracking-widest uppercase text-stone-900">Ágora</span>
    </div>

    <nav class="flex flex-col gap-2">
      <a href="/" class="px-4 py-2 rounded-lg text-sm font-medium text-stone-600 hover:bg-stone-200 hover:text-stone-900 transition-colors">
        Home
      </a>
      <a href="/notes" class="px-4 py-2 rounded-lg text-sm font-medium text-stone-600 hover:bg-stone-200 hover:text-stone-900 transition-colors">
        Notes
      </a>
      <a href="/docs" class="px-4 py-2 rounded-lg text-sm font-medium text-stone-600 hover:bg-stone-200 hover:text-stone-900 transition-colors">
        Documentation
      </a>
    </nav>
  </aside>

  <main class="flex-1 overflow-y-auto p-10 bg-white shadow-inner">
    {@render children()}
  </main>
</div>