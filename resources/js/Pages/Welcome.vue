<template>
    <Head title="Welcome" />

    <div class="pt-6 pb-16 sm:pb-24 lg:pb-32">
        <div>
            <nav class="relative flex  max-w-7xl mx-auto items-center justify-between px-4 sm:p-6">
                <div class="flex items-center flex-1">
                    <div class="flex items-center justify-between w-full md:w-auto">
                        <a href="">
                            <span class="sr-only">Laravel Community Tanzania</span>
                            <img class="h-12 w-auto sm:h-10" src="images/logo.png" alt="Laravel Community Tanzania">
                        </a>
                        <div class="flex -mr-2 items-center md:hidden">
                            <button
                                class="bg-white
                                     rounded-md
                                     p-2
                                     inline-flex
                                     items-center justify-center text-gray-400" type="button" >
                                <span class="sr-only">Open main menu</span>
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                                </svg>
                            </button><!--end of button-->
                        </div><!--end of Hardburg-->
                    </div><!--end of div hold the image-->

                    <div class="hidden md:block md:ml-10 md:space-x-10">
                        <a href="#" class="font-medium text-gray-500 hover:text-gray-900"> Home</a>
                        <a href="#" class="font-medium text-gray-500 hover:text-gray-900"> Developers</a>
                        <a href="#" class="font-medium text-gray-500 hover:text-gray-900"> Events</a>
                        <a href="#" class="font-medium text-gray-500 hover:text-gray-900"> Blog</a>
                    </div><!--end of menu-->
                </div><!--end of flex-1-->
                <div class="hidden md:block text-right">
                  <span class="inline-flex rounded-md shadow-md ring-1 ring-black ring-opacity-5">
                      <a href="#" class="inline-flex
                          items-center px-4 py-2
                          border border-transparent
                          text-base
                          font-medium rounded-md
                          text-primary-900 bg-white hover:bg-gray-50">Login</a>
                  </span>
                </div>
            </nav><!--end of nav-->

            <div>

            </div><!--end of popup-->
        </div><!--end of div-->
    </div><!--end of Main Div-->

</template>

<style scoped>

</style>

<script>
    import { defineComponent } from 'vue'
    import { Head, Link } from '@inertiajs/inertia-vue3';

    export default defineComponent({
        components: {
            Head,
            Link,
        },

        props: {
            canLogin: Boolean,
            canRegister: Boolean,
            laravelVersion: String,
            phpVersion: String,
        }
    })
</script>
