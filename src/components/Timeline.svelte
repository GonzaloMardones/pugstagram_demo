<script>
    import Card from './Card.svelte';
    import Loading from './Loading.svelte'
    export let posts = []
</script>

<!-- TimeLine.svelte -->
<style>
    .Timeline {
      padding: 4em 0 0 0;
    }
  </style>
  

<div class="Timeline">
    <div class="Timeline-container">
      {#each posts as post}
        <Card {...post}/>
      {:else}
        <Loading />
      {/each}
        
    </div>
</div>