<template>
  <!-- START:: HEADER -->
  <div class="p-4 md:ml-44 md:mr-40">
    <header
      class="flex justify-between items-center mb-5 md:mb-1 md:ml-9 md:mr-40"
    >
    <a href="https://tuaneka.com/dashboard">
      <div class="flex items-center gap-2 md:gap-7">
        <!-- Logo Image -->
        <img class="w-2/4" :src="logo" alt="Logo" />
        <!-- Frame272 Image -->
        <img class="w-4 md:w-6" :src="frame272" alt="Frame 272" />
      </div>
      </a>
      <div class="flex items-center md:space-x-5">
        <!-- Shopping Cart Image -->
        <img class="w-7" :src="frame66" alt="Frame 66" />
        <!-- my wallet Image -->
        <img class="w-32" :src="shoppingcart" alt="Shopping Cart" />

        <!-- Custom Dropdown -->
        <div class="relative">
          <div
            class="flex items-center justify-between bg-transparent cursor-pointer p-2"
          >
            <img class="w-5" src="/images/gh.png" alt="GH">
            <ChevronDown color="pink" fill="pink" />

          </div>
        </div>
      </div>
    </header>
  </div>
  <!-- END:: HEADER -->

  <nav className="flex justify-between ml-10 md:ml-56 mr-10 md:mr-60">
    <div className="flex gap-3 items-center">
      <h1
        className="bg-pink-600 w-6 h-6 flex justify-center items-center rounded-md"
      >
      <ArrowLeft color="white" fill="none" />
      </h1>
      <h1 className="font-semibold text-sm">Back</h1>
    </div>
    <div className="flex justify-center items-center">
      <img className="w-7 md:w-11" src="/images/avatar.png" />
      <hi className="font-semibold px-2">Ama</hi>
      <ChevronDown fill="black" />
    </div>
  </nav>  
  <div class="p-4 md:ml-44 md:mr-40">
   
    <MainPage />
    <!-- <ManualAi /> -->
  </div>
</template>

<script>
import { LucideAlertCircle, ChevronDown, ArrowLeft } from 'lucide-vue-next';

// Import the component
import MainPage from "./components/MainPage.vue";
import ManualAi from './components/ManualAi.vue';

export default {
  components: {
    LucideAlertCircle,
    ChevronDown,
    ArrowLeft,
    ManualAi,
    MainPage,
  },
  data() {
    return {
      // Assuming images are placed in the `public` folder
      logo: "/icons/logo.png", // Image path relative to public folder
      frame272: "/icons/Frame272.png", // Image path relative to public folder
      shoppingcart: "/icons/frame66.png", // Image path relative to public folder
      frame66: "/icons/shopping.png", // Image path relative to public folder
      dropdownOpen: false,
    };
  },
};
</script>

<style>
/* Custom dropdown styling */
.relative {
  position: relative;
}
</style>
