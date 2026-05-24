<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";

  const projects: {
    title: string;
    summary: string;
    href: string;
  }[] = [];
</script>

<Seo
  title="Jay Sarva - Projects"
  description="Selected projects by Jay Sarva."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Projects</h2>

  {#if projects.length === 0}
    <p class="text-lg text-neutral-500">Selected work may live here later.</p>
  {:else}
    <div class="grid gap-y-4">
      {#each projects as project}
        <a
          href={project.href}
          class="block -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors"
        >
          <div class="text-lg text-black">{project.title}</div>
          <div class="text-lg leading-snug font-serif italic">
            {project.summary}
          </div>
        </a>
      {/each}
    </div>
  {/if}
</section>
