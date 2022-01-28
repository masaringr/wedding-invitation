<template>
  <div class="flex h-screen md:p-12 p-6">
    <div
      class="flex flex-col md:flex-row h-full w-full rounded-2xl shadow-lg shadow-slate-300/30 backdrop-blur-[2px] bg-white/30 border-[3px] border-white/90 md:p-8 p-4 overflow-y-auto scrollbar-hide scroll-smooth"
    >
      <div
        class="md:h-full w-full flex justify-center items-center md:pr-8 border-b-2 md:border-b-0 border-white/90 pb-8 md:pb-0"
      >
        <transition appear @before-enter="beforeEnterImg1" @enter="enterImg1">
          <div class="w-96 hidden md:block">
            <vue-load-image>
              <template v-slot:image>
                <img class="drop-shadow w-full h-auto" :src="banner" alt="ari & fareta" />
              </template>
              <template v-slot:preloader>
                <img src="/image-loader.gif" />
              </template>
              <template v-slot:error>Image load fails</template>
            </vue-load-image>
          </div>
        </transition>

        <div class="relative md:hidden">
          <transition appear @before-enter="fromLeft" @enter="toCenter">
            <h4
              class="z-10 absolute top-10 left-2 text-2xl tracking-wide font-lusitana font-bold text-yellow-700/80 capitalize"
            >ari nugroho</h4>
          </transition>
          <transition appear @before-enter="beforeEnterImg1" @enter="enterImg1">
            <vue-load-image>
              <template v-slot:image>
                <img class="drop-shadow w-full h-auto" :src="banner" alt="ari & fareta" />
              </template>
              <template v-slot:preloader>
                <img src="/image-loader.gif" />
              </template>
              <template v-slot:error>Image load fails</template>
            </vue-load-image>
          </transition>
          <transition appear @before-enter="fromRight" @enter="toCenter">
            <h4
              class="z-10 absolute bottom-4 right-2 text-2xl tracking-wide font-lusitana font-bold text-yellow-700/80 capitalize"
            >fareta wahyu a</h4>
          </transition>
        </div>
      </div>
      <div class="md:h-full w-full flex flex-col justify-center items-center">
        <div class="md:border-l-[3px] border-white/90 md:pl-8">
          <div class="hidden md:flex flex-row w-full justify-center">
            <div class="pr-8 py-2 w-full border-r-[1.5px] border-white/90">
              <transition appear @before-enter="fromTop" @enter="toCenter">
                <h4
                  class="capitalize text-right tracking-wide font-lusitana leading-none text-2xl whitespace-nowrap font-bold text-yellow-700/80"
                >ari nugroho</h4>
              </transition>
            </div>
            <div class="pl-8 py-2 w-full border-l-[1.5px] border-white/90">
              <transition appear @before-enter="fromTop" @enter="toCenter">
                <h4
                  class="capitalize text-left tracking-wide font-lusitana leading-none text-2xl whitespace-nowrap font-bold text-yellow-700/80"
                >fareta wahyu a</h4>
              </transition>
            </div>
          </div>
          <div
            class="mt-8 mb-6 flex flex-col items-center border-b-2 md:border-b-0 border-white/90 pb-8 md:pb-0"
          >
            <transition appear @before-enter="beforeEnterAyat" @enter="enterAyat">
              <div class="flex flex-col items-center">
                <div class="w-12 border-t-[3px] border-slate-500/40 border-dotted mb-4"></div>
                <p class="text-center text-sm font-inter font-light text-slate-500/70">
                  "Dan Diantara tanda-tanda kebesaran-Nya ialah diciptakan-Nya untukmu pasangan hidup dari jenismu sendiri supaya kamu mendapatkan ketenangan hati dan dijadikan-Nya kasih sayang diantara kamu sesungguhnya yang demikian menjadi tanda-tanda kebesaran-Nya bagi orang-orang yang berfikir"
                  <br />
                  <br />(Surat Ar-Ruum:21)
                </p>
                <div class="w-12 border-t-[3px] border-slate-500/40 mt-4 border-dotted"></div>
              </div>
            </transition>
          </div>
          <div class="w-full md:pb-4 md:border-b-[3px] border-white/90 border-b-2 pb-8">
            <transition appear @before-enter="beforeEnterTgl1" @enter="enterTgl1">
              <div>
                <h3
                  class="text-2xl text-center font-lusitana font-bold text-yellow-700/80 tracking-wide"
                >24 & 25 Februari 2022</h3>
                <p
                  class="font-inter text-sm text-center text-slate-500/70"
                >Dusun Gamping, Desa Mojorejo, Mojokerto</p>
              </div>
            </transition>
          </div>
          <div class="md:mt-4 py-8 md:py-0 w-full flex flex-col md:flex-row gap-8 md:gap-0">
            <div
              class="md:pr-8 w-full md:border-r-[1.5px] border-white/90 pb-11 md:pb-0 border-b-2 md:border-b-0"
            >
              <transition appear @before-enter="fromBottom" @enter="toCenter">
                <div class="flex flex-col gap-2 justify-center items-center">
                  <div class="md:w-28 w-36">
                    <img
                      class="w-full h-auto rounded-xl shadow-slate-300/50"
                      src="/qr-lokasi.png"
                      alt="lokasi"
                    />
                  </div>
                  <div class="mt-2 md:mt-0">
                    <p
                      class="text-center font-inter text-sm md:text-xs text-slate-500/70"
                    >Scan untuk melihat lokasi, atau bisa klik tombol di bawah</p>
                  </div>
                  <div class="mt-4">
                    <a
                      href="https://goo.gl/maps/yMKdo6RFCcQ4J2XM7"
                      target="_blank"
                      class="capitalize font-semibold text-sm py-3 px-6 bg-sky-500 font-inter leading-none text-white rounded-lg hover:bg-sky-600 shadow-lg shadow-sky-500/50"
                    >lihat lokasi</a>
                  </div>
                </div>
              </transition>
            </div>
            <div class="h-48 md:h-auto md:pl-8 w-full md:border-l-[1.5px] border-white/90 relative">
              <transition appear @before-enter="fromBottom" @enter="toCenter">
                <div class="flex flex-col h-full justify-center items-center relative z-20">
                  <p class="text-center md:text-xs text-sm text-slate-500/70">
                    Ditunggu kehadirannya, teman-teman.
                    <span
                      class="text-xl block mt-2"
                    >&#128588;&#128588;&#129395;</span>
                  </p>
                </div>
              </transition>
              <div class="absolute top-0 w-full h-full">
                <canvas id="confetti" class="w-full h-full"></canvas>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { createToaster } from "@meforma/vue-toaster";
import gsap from "gsap"
import confetti from "https://cdn.skypack.dev/canvas-confetti@1";
import { onMounted } from "vue";
import VueLoadImage from 'vue-load-image';

const randomDirection = (min, max) => {
  return Math.random() * (max - min) + min;
}

const banner = '/banner.webp'

const showConfetti = () => {
  const canvas = document.getElementById('confetti');

  canvas.confetti = canvas.confetti || confetti.create(canvas, { resize: true });

  canvas.confetti({
    angle: randomDirection(55, 125),
    spread: randomDirection(50, 70),
    particleCount: randomDirection(50, 100),
    origin: { y: 1.2 }
  });
}

const runConfetti = onMounted(() => {
  setInterval(() => {
    showConfetti()
  }, 3000);
})

const beforeEnterImg1 = (el) => {
  el.style.opacity = 0
}

const enterImg1 = (el) => {
  gsap.to(el, {
    opacity: 1,
    duration: 3
  })
}

const beforeEnterTgl1 = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateY(-50px)'
}

const enterTgl1 = (el) => {
  gsap.to(el, {
    opacity: 1,
    y: 0,
    duration: 1,
    delay: 0.75
  })
}

const fromTop = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateY(-50px)'
}

const fromBottom = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateY(50px)'
}

const fromLeft = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateX(-50px)'
}

const fromRight = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateX(50px)'
}

const toCenter = (el) => {
  gsap.to(el, {
    opacity: 1,
    y: 0,
    x: 0,
    duration: 1,
  })
}

const beforeEnterAyat = (el) => {
  el.style.opacity = 0
  el.style.transform = 'translateY(-50px)'
}

const enterAyat = (el) => {
  gsap.to(el, {
    opacity: 1,
    y: 0,
    duration: 1,
    delay: 0.5
  })
}

const toaster = createToaster({
  position: "bottom",
  duration: 3000,
  dismissible: false,
  pauseOnHover: false
});

const copy = () => {
  const text = "1300017008908";
  navigator.clipboard.writeText(text).then(function () {
    toaster.show(`Copied : ${text}`);
  }, function (err) {
    console.error('Async: Could not copy text: ', err);
  });
}
</script>