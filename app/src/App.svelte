<script>
  import Window from './lib/Window.svelte';
  import src from './assets/xp.webp'
</script>

<div class="m">
  <img class="i" {src} alt="">
  <div class="c">
    <Window title="cat.png" />
  </div>
</div>

<style>
  .m {
    height: 100%;
    display: flex;
    aspect-ratio: 4 / 3;
    overflow: hidden;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  .m .i {
    object-fit: cover;
    display: flex;
    height: 100%;
    width: 100;
  }

  .m .c {
    z-index: 10;
    display: flex;
    height: 100%;
    aspect-ratio: 4 / 3;
    position: absolute;
    align-items: center;
    justify-content: center;
  }
</style>