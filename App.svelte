<script>
  import Button from "./Button.svelte";
  import Carousel from "./Carousel.svelte";
  let isShown = false;
  let images = [
    "https://i.imgur.com/cHNuyQr.jpeg",
    "https://i.imgur.com/Izh5ZHd.jpg",
    "https://i.imgur.com/5V73tPG.jpg",
    "https://i.imgur.com/uSKu6Fl.jpg"
  ];
  let hue = 4698;
  let carousel, n;
  $: if (carousel) carousel.go(n);
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
  .slide-content img {
    height: 50vh;
  }
</style>

<main>
	<h1>Hello CodeSandbox</h1>
	<h2>Start editing to see some magic happen!</h2>
	<Button />
  <br>
  <br>
  {#if isShown}
  <input type="range" step="1" min="0" max="3" bind:value={n} />
  <Carousel perPage="1" bind:this={carousel}>
  {#each images as image, i}
  <div class="slide-content">
  <img alt= {i} src= {image}>
 </div>
  {/each}
</Carousel>
{:else}
 <div 
 on:click={()=> isShown = true}
 on:mousemove={e => hue = e.clientX * e.clientY}
 style="background: hsl({hue / 500},100%, 50%); height:50vh"/>
{/if}
</main>