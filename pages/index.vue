<template>
  <section style="display: flex">
    <div>img src is resolved by webpack<img src="~/assets/square.svg" /></div>
    <div class="square-not-visible-1">URL is not resolved by webpack</div>
    <div class="square-not-visible-2">URL is not resolved by webpack</div>
    <div class="square-visible-1">Image is served from static</div>
    <div class="square-visible-2">Image is served from static</div>
  </section>
</template>

<style>
.square-not-visible-1 {
  min-width: 300px;
  min-height: 300px;
  background-image: url(~/assets/square.svg);
}
.square-not-visible-2 {
  min-width: 300px;
  min-height: 300px;
  background-image: url('/assets/square.svg');
}
.square-visible-1 {
  min-width: 300px;
  min-height: 300px;
  background-image: url(/square.svg);
}
.square-visible-2 {
  min-width: 300px;
  min-height: 300px;
  background-image: url('/square.svg');
}
</style>
