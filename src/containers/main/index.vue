<template>
  <section class="page-wrapper">
    <div class="title-box">
      <h1>{{ contentTitle }}</h1>
      <p>{{ contentDescription }}</p>
    </div>
  </section>
</template>

<script setup lang="ts">
import { CONTENT_PAGE } from '@common/content';
// variable
const contentTitle = CONTENT_PAGE.main.title;
const contentDescription = CONTENT_PAGE.main.description;
</script>

<style lang="scss">
.page-wrapper {
  @include flexSet(center, center, column);
  @include boxSet(100%, 100vh, 0px);
  @include colorSet(white, #111111);
}
.title-box {
  @include flexSet(center, center, column);
  gap: 10px;
  padding: 50px;
  & > h1 {
    @include fontSet(100px, 700, 110px);
    text-align: center;
    white-space: pre-wrap;
  }
}
</style>
