<script setup>
import { heroSectionContent, buttonsLabel } from "@/@core/constants/home-view";
import SiteButton from "@/@core/components/SiteButton.vue";
import { scrollToSection } from "@/@core/utils/functions";
</script>

<template>
  <section id="home" class="bg-hero-bg py-40 xl:py-44 3xl:py-56">
    <div class="container">
      <div class="grid lg:grid-cols-2 gap-20 3xl:gap-40">
        <div class="text-black">
          <h1 class="text-4.5xl xl:text-5xl 3xl:text-6xl font-bold">
            {{ heroSectionContent.heading }}
          </h1>
          <h3 class="text-2xl lg:text-3xl xl:text-4xl 3xl:text-4.5xl py-4 xl:pt-7 xl:pb-8">
            {{ heroSectionContent.subHeading }}
          </h3>
          <p class="text-base lg:text-xl xl:text-2xl 3xl:text-3xl">
            {{ heroSectionContent.text }}
          </p>

          <div class="flex gap-5 pt-12 lg:pt-20 xl:pt-24 3xl:pt-38">
            <SiteButton>
              {{ buttonsLabel.CTOBtn }}
            </SiteButton>
            <SiteButton outlined @click="scrollToSection('whyUs')">
              {{ buttonsLabel.whyUsBtn }}
            </SiteButton>
          </div>
        </div>
        <div class="flex items-end justify-center">
          <img :src="heroSectionContent.image" :alt="heroSectionContent.alt">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
header{
  background: theme('backgroundColor.hero-bg');
}
</style>