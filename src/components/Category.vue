<script setup>
  import category1 from "../assets/images/category/category1-img.webp"
  import category2 from "../assets/images/category/category2-img.webp"
  import category3 from "../assets/images/category/category3-img.webp"

  const categories = [
    {
      title: 'Сүнс',
      image: category1,
      desc: 'Сүнсний дүрд хувирагсад тоглолтын туршид өөрөө хонгилоор чөлөөтэй дамжих эрхтэй.'
    },
    {
      title: 'Шулам',
      image: category2,
      desc: 'Шуламны дүрд тоглогчид өөрсдийн шүүрийг ашиглан тулалдах боломжтой. Энэ тэдний тоглолтын туршид эдлэх давуу эрх болно.'
    },
    {
      title: 'Хулуун мангаа',
      image: category3,
      desc: 'Хулуу мангаа болсон оролцогчдод зориулан тоглолтын зарим бүсүүдэд хулуун их бууг байршуулсан бөгөөд зөвхөн тэд л ашиглаж чадна.'
    },
  ]
</script>

<template>
  <section id="category" class="flex flex-col items-center py-32">
    <h2 class="my-10 text-5xl md:text-6xl font-bold text-white">Ангилал</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 place-items-center">
      <div v-for="category of categories" :key="category.title" class="text-white grid place-items-center gap-5 text-center">
        <div class="p-10">
          <img :src="category.image" class="w-full" alt="category1">
        </div>
        <h3 class="text-3xl font-bold">{{ category.title }}</h3>
        <p class="w-3/4">{{ category.desc}}</p>
      </div>
    </div>
  </section>
  <section class="grid grid-flow-col grid-cols-1 md:grid-cols-2 md:gap-10 items-center">
    <div class="md:p-10">
      <img src="../assets/images/category2-img.webp" alt="category2-img">
    </div>
    <div class="text-center flex flex-col items-center">
      <h2 class="text-5xl md:text-6xl font-bold text-white">Сүнсний баяр</h2>
      <div class="flex items-center gap-5">
        <h2 class="text-5xl md:text-6xl font-bold text-white">гэж юу вэ?</h2>
        <img src="../assets/images/head2-img.png" class="w-9 md:w-12" alt="head2">
      </div>
      <p class="mt-8 md:mt-12 text-white text-lg md:text-xl w-full md:w-[80%]">Halloween бол жил бүрийн 10-р сарын 31-нд тэмдэглэдэг баяр бөгөөд 2023 оны Halloween 10-р сарын 31-ний Мягмар гаригт тохионо. Энэ уламжлал нь эртний Кельтүүдийн Самхайн баяраас үүдэлтэй бөгөөд хүмүүс гал асааж, сүнсийг хамгаалах хувцас өмсдөг байв.</p>
    </div>
  </section>
</template>