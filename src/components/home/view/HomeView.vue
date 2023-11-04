<template>
  <div class="wrap min-h-screen dark:bg-neutral-900">
    <div class="main flex justify-center items-center p-8">
      <div class="content flex flex-col gap-4 md:gap-16 lg:gap-24">
        <navigation-bar />

        <div class="wrap flex justify-center">
          <div class="body flex flex-col gap-4 md:gap-8 lg:gap-8 w-full md:w-7/12 lg:w-7/12">
            <div class="full-name flex flex-col">
              <p class="text-3xl font-bold tracking-tight dark:text-gray-100">Talgat Sovetbekov</p>
              <label class="text-base font-normal text-neutral-500 dark:text-neutral-400">Software Engineer at <span class="hover:text-rose-500">@kaspi.kz</span></label>
            </div>
            <div class="short-intro flex flex-col md:flex-row lg:flex-row gap-4 md:gap-8 lg:gap-8">
              <img src="../../../assets/talgat.jpg" class="rounded-full" width="93px">
              <div class="whoami flex flex-col gap-2 m-1">
                <p class = "text-neutral-700 dark:text-neutral-200">Build software <span class="hover:text-rose-500">@kaspi.kz</span> during the day. Other times, I read, go to the gym, periodically get lost in Spotify and do a lil bit of climbing.</p>
                <p class = "text-neutral-500   dark:text-neutral-400">Almaty, Kazakhstan</p>
              </div>
            </div>
            <div class="contacts">
              <ul class="list-none flex flex-col md:flex-row lg:flex-row gap-4 md:gap-8 lg:gap-8 text-base text-neutral-500 dark:text-neutral-400">
                <li class="flex flex-row gap-3">
                  <i class="pi pi-arrow-up-right mt-1" />
                  <p>Email me</p>
                </li>
                <li class="flex flex-row gap-3">
                  <i class="pi pi-arrow-up-right mt-1" />
                  <p>More ways to connect</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import 'primeicons/primeicons.css';
import NavigationBar from '../components/NavigationBar.vue'

</script>
<style scoped >

</style>
