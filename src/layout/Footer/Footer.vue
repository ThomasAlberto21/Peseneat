<script setup>
import PagesList from './PagesList.vue'
import ContactList from './ContactList.vue'
import LegalList from './LegalList.vue'
import SocialMediaList from './SocialMediaList.vue'
import { RouterLink } from 'vue-router'
import { footer } from '../../constants/constants'
</script>

<template>
  <footer class="bg-black">
    <div class="w-full max-w-screen-xl p-4 py-6 mx-auto lg:py-8">
      <div class="xl:flex xl:justify-between">
        <div class="mb-6 md:mb-10 xl:mr-20">
          <h2 class="mb-5 text-base font-semibold text-white">
            Download the app by clicking the link below
          </h2>
          <div class="flex gap-2">
            <RouterLink to="/">
              <img
                src="/images/google_play.png"
                class="h-auto bg-center bg-no-repeat bg-cover w-52"
                alt="Google Play"
              />
            </RouterLink>
            <RouterLink to="/">
              <img
                src="/images/app_store.png"
                class="h-auto bg-center bg-no-repeat bg-cover w-52"
                alt="App Store"
              />
            </RouterLink>
          </div>
        </div>

        <div class="grid grid-cols-1 gap-8 sm:gap-6 sm:grid-cols-3">
          <!-- Pages -->
          <PagesList :footer="footer" />

          <!-- Contact -->
          <ContactList :footer="footer" />

          <!-- Legal -->
          <LegalList :footer="footer" />
        </div>
      </div>
      <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />

      <!-- Social Media -->
      <SocialMediaList :footer="footer" />
    </div>
  </footer>
</template>
<script>
export default {
  name: 'FooterComponent'
}
</script>
