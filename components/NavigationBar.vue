<template>
  <section>
    <header class="bg-[#F3F5F6]">
      <div class="mx-auto max-w-screen-xl px-4 sm:px-6 lg:px-8">
        <div class="flex h-16 items-center justify-between">
          <div class="md:flex md:items-center md:gap-12">
            <a class="block text-teal-600" href="/">
              <span class="sr-only">Home</span>
              <img src="@/assets/img/new-logo.png" alt="" class="h-12">
            </a>
          </div>

          <div class="hidden md:block">
            <nav aria-label="Global">
              <ul class="flex items-center gap-6 text-sm">
                <li>
                  <nuxt-link exact="" class="text-[#1E1E1E] transition hover:text-gray-500/75" to="/">
                    Home
                  </nuxt-link>
                </li>

                <li>
                  <nuxt-link exact="" class="text-[#1E1E1E] transition hover:text-gray-500/75" to="/">
                    About
                  </nuxt-link>
                </li>

                <li>
                  <nuxt-link exact="" class="text-[#1E1E1E] transition hover:text-gray-500/75" to="/">
                    Services
                  </nuxt-link>
                </li>
                <li>
                  <a
                    class="text-[#1E1E1E] transition hover:text-gray-500/75"
                    href="https://medinize-communities.netlify.app/"
                    target="_self"
                  >Community</a>
                </li>

                <li>
                  <nuxt-link exact="" class="text-[#1E1E1E] transition hover:text-gray-500/75" to="/faq">
                    FAQs
                  </nuxt-link>
                </li>

                <li>
                  <nuxt-link exact="" class="text-[#1E1E1E] transition hover:text-gray-500/75" to="/">
                    Contact
                  </nuxt-link>
                </li>
              </ul>
            </nav>
          </div>

          <div class="flex items-center gap-4">
            <div class="sm:flex sm:gap-4">
              <div class="hidden sm:flex">
                <a href="https://medinize-communities.netlify.app/"
                  class="rounded-full px-5 py-2.5 text-sm font-medium text-gray-600 border-2 border-[#13B859] shadow"
                >
                  Login
                </a>
              </div>
              <div class="hidden sm:flex">
                <a href="https://medinize-communities.netlify.app/signup" class="rounded-full bg-[#13B859] text-white px-5 py-2.5 text-sm font-medium" to="/sign-up">
                  Sign Up
                </a>
              </div>
            </div>

            <div class="block md:hidden">
              <button
                class="rounded bg-gray-100 p-2 text-gray-600 transition hover:text-gray-600/75"
                @click="showNavbar = !showNavbar"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
              </button>
            </div>
          </div>
        </div>
      </div>
    </header>
    <div class="w-11/12 mx-auto">
      <section v-if="showNavbar" class="absolute top-2 bg-black lg:hidden z-50 w-11/12 mx-auto rounded-lg p-6 space-y-6">
        <div class="flex justify-between items-center">
          <div><img src="@/assets/img/new-logo.png" alt="" class="h-"></div>
          <div class="rounded-full cursor-pointer bg-white shadow-lg p-2 px-3" @click="showNavbar = !showNavbar">
            X
          </div>
        </div>
        <ul class="space-y-6 z-50">
          <li>
            <a href="https://medinize-communities.netlify.app/" class="text-white font-medium">
              Login
            </a>
          </li>
          <div class="pt-6">
            <a href="https://medinize-communities.netlify.app/signup" class="text-white w-full bg-green-400 rounded-md px-20 py-2.5">
              Sign
              Up
            </a>
          </div>
        </ul>
      </section>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      showNavbar: false
    }
  }
}
</script>

<style scoped>
.nuxt-link-exact-active {
  font-weight: bold;
  color: blue;
}
</style>
