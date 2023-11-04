<template>
  <div class="header flex justify-between mx-4 md:mx-16 lg:mx-52">
      <div></div>
      <div>
      <ul class="list-none flex flex-col md:flex-row lg:flex-row gap-4 md:gap-16 lg:gap-16 text-sm dark:text-neutral-400 text-neutral-600">
           <li class="cursor-pointer dark:hover:text-neutral-200 hover:text-black">About</li>
           <li class="cursor-pointer dark:hover:text-neutral-200 hover:text-black">Contacts</li>
           <li class="cursor-pointer dark:hover:text-neutral-200 hover:text-black">Gear</li>
      </ul>
      </div>
      <div class="flex dark:text-neutral-500 cursor-pointer">
         <i :class="darkMode ? 'pi pi-moon' : 'pi pi-sun'" @click="toggleDarkMode()"/>
      </div>
  </div>
</template>
<script setup lang="ts">
import 'primeicons/primeicons.css';
import { ref, onMounted } from 'vue';

const darkMode = ref(false)

// Load dark mode preference from local storage on component mount
onMounted(() => {
  const isDarkMode = localStorage.getItem('darkMode');
  if (isDarkMode) {
    darkMode.value = isDarkMode === 'true';
    applyDarkMode(darkMode.value);
  }
});

const toggleDarkMode = () => {
  darkMode.value = !darkMode.value;
  applyDarkMode(darkMode.value);
  localStorage.setItem('darkMode', darkMode.value.toString());
}

const applyDarkMode = (isDarkMode: boolean) => {
  const html = document.documentElement;
  html.classList.toggle('dark', isDarkMode);
}
</script>
<style scoped>

</style>
