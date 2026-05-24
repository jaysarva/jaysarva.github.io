<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import BlogList from "./BlogList.svelte";
  import posts from "./posts.yaml";
</script>

<Seo
  title="Jay Sarva - Blog"
  description="Technical writing by Jay Sarva on information retrieval, agentic search, dense retrieval, and related ideas."
/>

<section class="layout-md py-12">
  <h2 class="heading2">Thoughts</h2>
  <BlogList data={posts} />
</section>
