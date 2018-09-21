<template>
  <section style="display: flex;">
    <div>img src is resolved by webpack ~/assets/<img src="~/assets/square.svg" /></div>
    <div>img src is resolved by webpack ~assets/<img src="~assets/square.svg" /></div>
    <div class="square-not-visible-1">URL is not resolved by webpack~/assets/</div>
    <div class="square-not-visible-2">URL is not resolved by webpack ~/assets/</div>
    <div class="square-visible-1">URL is resolved by webpack ~assets/</div>
    <div class="square-visible-2">URL is resolved by webpack ~assets/</div>
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
  background-image: url('~/assets/square.svg');
}
.square-visible-1 {
  min-width: 300px;
  min-height: 300px;
  background-image: url(~assets/square.svg);
}
.square-visible-2 {
  min-width: 300px;
  min-height: 300px;
  background-image: url('~assets/square.svg');
}
</style>
