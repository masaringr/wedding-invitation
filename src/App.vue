<template>
  <div class="flex h-screen md:p-12 p-6">
    <div
      class="flex flex-col md:flex-row h-full w-full rounded-2xl shadow-lg shadow-slate-300/30 backdrop-blur-[2px] bg-white/30 border-[3px] border-white/90 md:p-8 p-4 overflow-y-auto scrollbar-hide"
    >
      <div
        class="md:h-full w-full flex justify-center items-center md:pr-8 border-b-2 md:border-b-0 border-white/90 pb-8 md:pb-0"
      >
        <div class="w-96 hidden md:block">
          <img class="drop-shadow w-full h-auto" src="/banner.png" alt="ari & fareta" />
        </div>

        <div class="relative md:hidden">
          <h4
            class="z-10 absolute top-4 left-2 text-2xl tracking-wide font-lusitana font-bold text-yellow-700/80 capitalize"
          >ari nugroho</h4>
          <img class="drop-shadow w-full h-auto" src="/banner.png" alt="ari & fareta" />
          <h4
            class="z-10 absolute -bottom-2 right-2 text-2xl tracking-wide font-lusitana font-bold text-yellow-700/80 capitalize"
          >fareta wahyu a</h4>
        </div>
      </div>
      <div
        class="md:h-full w-full flex flex-col justify-center items-center md:border-l-[3px] border-white/90 md:pl-8"
      >
        <div class="hidden md:flex flex-row w-full justify-center">
          <div class="pr-8 py-2 w-full border-r-[1.5px] border-white/90">
            <h4
              class="capitalize text-right tracking-wide font-lusitana leading-none text-2xl whitespace-nowrap font-bold text-yellow-700/80"
            >ari nugroho</h4>
          </div>
          <div class="pl-8 py-2 w-full border-l-[1.5px] border-white/90">
            <h4
              class="capitalize text-left tracking-wide font-lusitana leading-none text-2xl whitespace-nowrap font-bold text-yellow-700/80"
            >fareta wahyu a</h4>
          </div>
        </div>
        <div
          class="mt-8 mb-6 flex flex-col items-center border-b-2 md:border-b-0 border-white/90 pb-8 md:pb-0"
        >
          <div class="w-12 border-t-[3px] border-slate-500/40 border-dotted mb-4"></div>
          <p class="text-center text-sm font-inter font-light text-slate-500/70">
            "Dan Diantara tanda-tanda kebesaran-Nya ialah diciptakan-Nya untukmu pasangan hidup dari jenismu sendiri supaya kamu mendapatkan ketenangan hati dan dijadikan-Nya kasih sayang diantara kamu sesungguhnya yang demikian menjadi tanda-tanda kebesaran-Nya bagi orang-orang yang berfikir"
            <br />
            <br />(Surat Ar-Ruum:21)
          </p>
          <div class="w-12 border-t-[3px] border-slate-500/40 mt-4 border-dotted"></div>
        </div>
        <div class="w-full md:pb-4 md:border-b-[3px] border-white/90 border-b-2 pb-8">
          <h3
            class="text-2xl text-center font-lusitana font-bold text-yellow-700/80 tracking-wide"
          >24 Februari 2022</h3>
          <p
            class="font-inter text-sm text-center text-slate-500/70"
          >Dusun Gamping, Desa Mojorejo, Mojokerto</p>
        </div>
        <div class="md:mt-4 py-8 md:py-0 w-full flex flex-col md:flex-row gap-8 md:gap-0">
          <div
            class="md:pr-8 w-full md:border-r-[1.5px] border-white/90 pb-11 md:pb-0 border-b-2 md:border-b-0"
          >
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
          </div>
          <div class="md:pl-8 w-full md:border-l-[1.5px] border-white/90">
            <div class="flex flex-col h-full justify-center items-center">
              <div class="p-2 border-[3px] border-rose-500 mb-2">
                <h4
                  class="uppercase whitespace-nowrap font-inter text-base leading-none font-semibold text-rose-500"
                >space available</h4>
              </div>
              <p class="text-center md:text-xs text-sm text-slate-500/70 mb-2">
                Ga deng, becanda. ini karena ga tau mau diisi apa
                <br />
                <span class="text-base block">&#128513;</span>
              </p>
              <p class="text-center md:text-xs text-sm text-slate-500/70">
                Ditunggu kehadirannya, teman-teman.
                <span
                  class="text-base block"
                >&#128588;&#128588;&#129395;</span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { createToaster } from "@meforma/vue-toaster";

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