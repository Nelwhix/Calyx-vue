<template>
   <main class="px-16 py-6 bg-gray-100 md:col-span-6">
        <div class="flex justify-center md:justify-end mb-10">
                <a href="#" class="text-primary btn">Login</a>
                <a href="#" class="text-primary ml-2 btn">Sign up</a>
        </div>

        <header>
            <h2 class="relative text-gray-700 text-6xl font-semibold heroText">Discover<span class="cursor">_</span></h2>
            <h4 class="text-gray-700">You can come eat in, or get your food delivered to your doorsteps</h4>
        </header>
        <div>
                <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">Popular menu items</h4>

                <div class="mt-8 grid lg:grid-cols-3 gap-10">
                    <!-- menu cards go here -->
                    <div class="card hover:shadow-lg">
                        <img src="../assets/Images/jollof.jpg" alt="jollof" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                            <span class="font-bold">Party Jollof Rice</span>
                        </div>
                        <div class="badge">
                            <svg class="w-5 inline-block h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>25 mins</span>
                        </div>
                    </div>
                    <div class="card hover:shadow-lg">
                        <img src="../assets/images/friedrice.jpg" alt="friedrice" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                            <span class="font-bold">Fried rice</span>
                        </div>
                        <div class="badge">
                            <svg class="w-5 inline-block h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>20 mins</span>
                        </div>
                    </div>
                    <div class="card hover:shadow-lg">
                        <img src="../assets/images/egusi.jpg" alt="egusi" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                            <span class="font-bold">Pounded Yam & Eguisi soup</span>
                        </div>
                        <div class="badge">
                            <svg class="w-5 inline-block h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>40 mins</span>
                        </div>
                    </div>
                </div>


                <div class="flex justify-center mt-3">
                    <div class="bg-secondary-100 btn hover:shadow-inner transform hover:scale-125 hover:bg-opacity-50 transition ease-out duration-300">Load more</div>
                </div>
         </div>

        <section class="my-10">
            <h4 class=" text-2xl text-gray-700 text-center font-semibold">About Us</h4>
            <p class="font-body mt-5">Calyx was started 4 years ago with the simple goal of providing home-cooked meals and top notch customer experiences
                in Warri Mall, Effrun. Among the shops at Food Court Warri, we are always clearly #1. Our staff always have smiles on
                their faces and our customers too.
            </p>
             <div class="flex justify-center mt-3">
                <div class="bg-secondary-100 btn hover:shadow-inner transform hover:scale-125 hover:bg-opacity-50 transition ease-out duration-300"><router-link to="/about">Read more</router-link></div>
            </div>
        </section>
        </main>
</template>

<script>
import { gsap } from "gsap";
import { RoughEase } from "gsap/EasePack";
import { TextPlugin } from "gsap/TextPlugin";
import { withModifiers } from "vue";

export default {
  data() {
    return {
      heroText : 'Discover tasty meals unforgettable experiences at Calyx Restaurant'
    }
  },
  mounted() {
    gsap.registerPlugin(TextPlugin);
    gsap.to('.cursor', {opacity: 0, ease: "Power1.inOut", repeat: -1});
    gsap.timeline().to('.heroText', {duration: 5, text: this.heroText, delay: 0.5})
  }
}
</script>