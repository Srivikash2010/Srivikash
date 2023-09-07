<template>
  <div>
    <header class="absolute inset-x-0 top-0 z-50">
      <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="/" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="h-8 w-auto" src="data:image/png;base64,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" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation" :key="item.name" :href="item.href" class="text-sm font-semibold leading-6 text-gray-900">{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <a href="/product" class="text-sm font-semibold leading-6 text-gray-900">Try out our first product! <span aria-hidden="true">&rarr;</span></a>
        </div>
      </nav>
      <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="flex items-center justify-between">
            <a :href="'/'" class="-m-1.5 p-1.5">
              <span class="sr-only">Recycle</span>
              <img class="h-8 w-auto" src="data:image/png;base64,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" alt="" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
              </div>
              <div class="py-6">
                <a href="/product" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Try our product</a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
  { name: 'Our Product', href: '/product' },
  { name: 'About Us', href: '#' },
  { name: 'Marketplace', href: '#' },
  { name: 'Company', href: '/company' },
]

const mobileMenuOpen = ref(false)
</script>



<style>

</style>
