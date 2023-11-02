<script lang="ts">
  import { graphql } from "$houdini";

  const carsList = graphql(`
    query CarsList @load {
      cars(limit: 1) {
        status
        title
        condition
      }
    }
  `);
</script>

<h1>Welcome to SvelteKit</h1>
{JSON.stringify($carsList, null, 2)}
