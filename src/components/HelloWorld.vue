<script setup>
import { ref } from 'vue';
import { CaptionableImage } from './CaptionableImage.vue';

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>

  <CaptionableImage
    src="https://placekitten.com/400/300"
    alt="test"
    title="test"
    caption="This is a caption"
  />
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
