<script setup lang="ts">
import { themeChange } from 'theme-change';

onMounted(() => {
  themeChange(false);
});

const arr = [
  'winter',
  'night',
  'cupcake',
  'synthwave',
  'forest',
  'aqua',
  'dracula',
];
</script>

<template>
  <div class="p-4">
    <button class="btn">Hello daisyUI</button>
    <select data-choose-theme>
      <option :value="item" v-for="item in arr">{{ item }}</option>
    </select>
    <div class="card w-96 bg-base-100 shadow-xl">
      <figure>
        <img src="https://placeimg.com/400/225/arch" alt="Shoes" />
      </figure>
      <div class="card-body">
        <h2 class="card-title">Shoes!</h2>
        <p>If a dog chews shoes whose shoes does he choose?</p>
        <div class="card-actions justify-end">
          <button class="btn btn-primary">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</template>
