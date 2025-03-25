<script setup>
  const isOpen = ref(false);

  const openNow = () => {
    isOpen.value = true;
  }
</script>

<template>
  <div class="flex items-center justify-center h-screen">
    <div v-if="!isOpen" class="flex flex-col items-center gap-5">
      <h1 class="text-4xl font-bold">Open it here 👇</h1>
      <div class="text-center">
        <button type="button" @click="openNow" class="focus:outline-none text-white bg-red-500 hover:bg-red-600 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-800">
          OPEN NOW
        </button>
      </div>
    </div>
    <!-- Result -->
     <div v-if="isOpen">
        <h1 class="text-4xl font-bold">🎉 Congrats! You've opened it 🎉</h1>
        <!-- show image gif I love you -->
         <img src="/images/i-love-u.gif" alt="Hey, ♥ I love you ♥" class="object-cover" />
     </div>
  </div>
</template>
