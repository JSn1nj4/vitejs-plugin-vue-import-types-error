<template>
  <figure class="relative block overflow-hidden rounded-lg">
    <img
      class="relative mx-auto object-contain"
      :src="src"
      :alt="alt"
      :title="title"
      :srcset="srcset"
    />
    <figcaption
      v-if="caption"
      class="
        caption
        absolute
        bottom-0
        left-0
        block
        w-full
        p-4
        text-center
        bg-black/30
      "
    >
      {{ caption }}
    </figcaption>
  </figure>
</template>

<script setup lang="ts">
import { ImageWithCaption } from './ImageTypes';

const props = defineProps<ImageWithCaption>();
</script>
