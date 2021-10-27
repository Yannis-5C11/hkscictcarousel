<script>
  import Button from "./Button.svelte";
  import Carousel from "./Carousel.svelte";
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
  <Carousel perPage="1">
  <div class="slide-content">
  <img alt="1" src="https://i.imgur.com/cHNuyQr.jpeg">
 </div>
  <div class="slide-content">
  <img alt="2" src="https://i.imgur.com/Izh5ZHd.jpg">
  </div>
  <div class="slide-content">
   <img alt="3" src="https://i.imgur.com/5V73tPG.jpg">
  </div>
  <div class="slide-content">
   <img alt="4" src="https://i.imgur.com/uSKu6Fl.jpg">
  </div>
</Carousel>
</main>