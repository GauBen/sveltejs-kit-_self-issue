<script lang="ts">
  import { onMount } from 'svelte';

  let mounted = false
  onMount(() => {
    mounted = false;
    setTimeout(() => {
      mounted = true;
    }, 200)
  })
</script>

<slot/>

<div>{mounted ? 'mounted' : 'loading...'}</div>
