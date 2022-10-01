<script setup>
import { vAutoAnimate } from '@formkit/auto-animate';
import { useAutoAnimate } from '@formkit/auto-animate/vue';
import { ref } from 'vue';

const isOpen = ref(false);
const [wrapperEl] = useAutoAnimate();
</script>

<template>
  <div
    v-auto-animate="{ duration: 1000, easing: 'linear' }"
    class="p-8 rounded-lg bg-neutral-900"
  >
    <h2 class="text-xl font-bold" @click="isOpen = !isOpen">
      Why you should subscribe
    </h2>
    <p v-if="isOpen" class="py-8">I'm close to 20k so please 🙏</p>
  </div>
  <!-- <div ref="wrapperEl" class="p-8 rounded-lg bg-neutral-900">
    <h2 class="text-xl font-bold" @click="isOpen = !isOpen">
      Why you should subscribe
    </h2>
    <p v-if="isOpen" class="py-8">I'm close to 20k so please 🙏</p>
  </div> -->
</template>
