<template>
    <div class="transition-all duration-500 md:col-span-1 md:flex md:justify-end" :class="{'scrolled-nav': scrollPosition }">
      <nav class="text-right transition-all duration-500">
        <div class="flex justify-between items-center">
          <h1 class="p-4 border-b border-gray-100">
            <router-link to="/">
              <img src="../assets/Images/logo.png" alt="" class="transition-all duration-500">
            </router-link>
          </h1>
            <div class="burger">
              <svg @click="toggleMobileNav" class="h-6 w-6  transition-transform duration-500 active:rotate-90" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
              </svg>
            </div>
        </div> 
        <ul v-show="!mobile" class="text-sm mt-6 hidden md:block navigation">
          <li class="py-1">
            <router-link to="/" class="px-4 flex justify-end border-r-4 border-primary">
              <span class="">Home</span>
              <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
              </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/menu" class="px-4 flex justify-end border-r-4 border-white">
              <span class="">Menu</span>
                <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" />
                </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/about" class="px-4 flex justify-end border-r-4 border-white">
            <span class="">About</span>
            <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/contact" class="px-4 flex justify-end border-r-4 border-white">
            <span>Contact</span>
            <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            </router-link>
        </li>
      </ul>   
      <transition name="mobile-nav">
        <ul v-show="mobileNav" class="text-sm mt-6">
          <li class="py-1">
            <router-link to="/" class="px-4 flex justify-end border-r-4 border-primary">
              <span class="">Home</span>
              <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
              </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/menu" class="px-4 flex justify-end border-r-4 border-white">
              <span class="">Menu</span>
                <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" />
                </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/about" class="px-4 flex justify-end border-r-4 border-white">
            <span class="">About</span>
            <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            </router-link>
          </li>
          <li class="py-1">
            <router-link to="/contact" class="px-4 flex justify-end border-r-4 border-white">
            <span>Contact</span>
            <svg class="w-5 ml-2 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            </router-link>
        </li>
        </ul> 
      </transition>
      </nav>
    </div>  
</template>

<script>
export default {
  name: "navigation",
  data() {
    return { 
      scrollPosition: null,
      mobile: false,
      mobileNav: false,
      windowWidth: null,
    };
  },
  methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav
    }
  }
}
</script>
