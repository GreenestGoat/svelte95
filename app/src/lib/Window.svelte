<script>
  import { draggable } from '@neodrag/svelte';

  export let title = 'window';
</script>

<div class="w" use:draggable={{ handle: '.h', gpuAcceleration: true, bounds: 'parent' }}>
  <div class="h">
    <span>{title}</span>
  </div>
  <div class="c">
    <slot></slot>
  </div>
</div>
  
<style>
  .w {
    min-height: 300px;
    min-width: 500px;
    max-height: 300px;
    max-width: 500px;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: flex-start;
    border-top: 2px solid white;
    border-left: 2px solid white;
    border-right: 2px solid #393939;
    border-bottom: 2px solid #393939;
    border-radius: 0;
    background: #C0C0C0;
    padding: 1px;
    box-sizing: border-box;
    line-height: 1.5;
    z-index: 2;
  }

  .w .h {
    font-size: .65rem;
    padding: 4px;
    color: #C9C9C9;
    border-radius: 0;
    border: 2px solid #BDBDBD;
    width: 100%;
    display: flex;
    background-color: #000181;
    color: white;
    box-sizing: border-box;
    align-items: center;
    text-align: left;
    height: 32px;
    cursor: move;
    padding: .75rem .5rem;
    font-weight: 100;
    margin-bottom: 0;
  }

  .w .c {
    width: 100%;
    display: flex;
    box-sizing: border-box;
    align-items: center;
    text-align: left;
    height: 100%;
    overflow: hidden;
    padding: 2px;
  }
</style>