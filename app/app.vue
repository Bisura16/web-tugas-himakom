<script setup>
// 1. Data Sosial Media
const socialLinks = [
  {
    name: 'LinkedIn',
    icon: 'mdi:linkedin',
    url: 'https://www.linkedin.com/in/bimo-surya-anggara?utm_source=share_via&utm_content=profile&utm_medium=member_ios'
  },
  {
    name: 'Instagram',
    icon: 'mdi:instagram',
    url: 'https://www.instagram.com/suryangraa?igsh=MXRram1yOXM2NzU0NA%3D%3D&utm_source=qr'
  },
  {
    name: 'GitHub',
    icon: 'mdi:github',
    url: 'https://github.com/Bisura16'
  }
]

// 2. Data Skill
const skillCategories = [
  {
    title: 'Programming Language',
    skills: [
      { name: 'Python', icon: 'vscode-icons:file-type-python' },
      { name: 'SQL', icon: 'logos:postgresql' },
      { name: 'C Language', icon: 'logos:c' }
    ]
  },
  {
    title: 'Tools',
    skills: [
      { name: 'Microsoft Excel', icon: 'vscode-icons:file-type-excel' },
      { name: 'VS Code', icon: 'devicon:vscode' }
    ]
  },
  {
    title: 'Other Interests',
    skills: [
      { name: 'Financial Analysis', icon: 'mdi:finance' },
      { name: 'Football', icon: 'streamline-cyber-color:football' },
      { name: 'Someone', icon: 'icon-park:women' }
    ]
  }
]

// 3. Data Sertifikat
const certificates = [
  {
    title: 'Sertifikat Ketua Divisi Multimedia',
    issuer: 'SMAN 1 TAMBUN SELATAN',
    date: '2024 - 2025',
    image: '/cert1.jpg',
    description: 'Menjabat sebagai ketua divisi Multimedia periode 2024 - 2025'
  },
  {
    title: 'Sertifikat IOS KIMIA',
    issuer: 'Platform olimpiade online',
    date: '2024',
    image: '/cert2.jpg',
    description: 'Mengikuti olimpiade online pada tahun 2024'
  }
]
</script>

<template>
  <div class="min-h-screen bg-[#030712] text-white font-sans scroll-smooth selection:bg-indigo-500/30">
    <nav class="sticky top-0 z-50 bg-[#030712]/70 backdrop-blur-xl border-b border-white/5 py-4">
      <div class="container mx-auto px-6 flex justify-between items-center">
        <h1 class="text-2xl font-black tracking-tighter">
          Bimo<span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-indigo-500">.Dev</span>
        </h1>
        <div class="hidden md:flex space-x-8 text-sm font-bold text-slate-400">
          <a href="#beranda" class="hover:text-white transition-colors">Beranda</a>
          <a href="#profil" class="hover:text-white transition-colors">Profil</a>
          <a href="#skill" class="hover:text-white transition-colors">Skill</a>
          <a href="#penugasan" class="hover:text-white transition-colors">Penugasan</a>
          <a href="#kontak"
            class="bg-gradient-to-r from-blue-600 to-indigo-600 text-white px-5 py-2 rounded-full hover:scale-105 transition-transform shadow-lg shadow-indigo-500/20">Kontak</a>
        </div>
      </div>
    </nav>

    <section id="beranda" class="min-h-[95vh] flex items-center relative overflow-hidden py-20">
      <div
        class="absolute top-0 left-0 w-[600px] h-[600px] bg-blue-600/20 rounded-full blur-[140px] -translate-x-1/2 -translate-y-1/2">
      </div>
      <div
        class="absolute bottom-0 right-0 w-[600px] h-[600px] bg-indigo-600/20 rounded-full blur-[140px] translate-x-1/2 translate-y-1/2">
      </div>
      <div class="container mx-auto px-6 z-10 flex flex-col md:flex-row items-center gap-16">
        <div class="md:w-3/5">
          <div class="inline-flex items-center gap-2 bg-white/5 border border-white/10 px-4 py-1.5 rounded-full mb-6">
            <span class="w-2 h-2 bg-blue-500 rounded-full animate-ping"></span>
            <span class="text-xs font-bold tracking-widest text-slate-300 uppercase">Available for Projects</span>
          </div>
          <h2 class="text-6xl md:text-8xl font-black mb-6 leading-[1.1] tracking-tight">
            Bimo Surya <br>
            <span
              class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 via-indigo-400 to-purple-500">Anggara</span>
          </h2>
          <p class="text-xl md:text-2xl font-medium text-slate-400 mb-10 leading-relaxed max-w-xl">
            Halo, saya Bimo Surya Anggara, <span class="text-white font-bold">Mahasiswa D4 Teknik Informatika
              POLBAN.</span> Saat ini saya sedang fokus menekuni skill dibidang data untuk menjadi seorang <span
              class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-indigo-400 font-bold">data
              analyst.</span>
          </p>
          <div class="flex gap-6 mb-12">
            <a v-for="link in socialLinks" :key="link.name" :href="link.url" target="_blank"
              class="text-2xl text-slate-500 hover:text-blue-400 hover:-translate-y-1 transition-all">
              <Icon :name="link.icon" />
            </a>
          </div>
          <div class="flex flex-wrap gap-5">
            <a href="#penugasan"
              class="group bg-white text-black px-10 py-4 rounded-full font-black hover:bg-gradient-to-r from-blue-500 to-indigo-600 hover:text-white transition-all duration-300 flex items-center gap-2 shadow-xl shadow-white/5">
              Lihat Karya
              <Icon name="material-symbols:arrow-right-alt" class="group-hover:translate-x-2 transition-transform" />
            </a>
            <a href="#kontak"
              class="border border-white/10 bg-white/5 backdrop-blur-md px-10 py-4 rounded-full font-black hover:bg-white/10 transition-all">Kontak
              Saya</a>
          </div>
        </div>
        <div class="md:w-2/5 flex justify-center">
          <div class="relative group p-4 bg-white/5 border border-white/10 rounded-[2.5rem] backdrop-blur-2xl">
            <div class="w-72 h-[450px] md:w-80 md:h-[520px] rounded-[2rem] overflow-hidden relative shadow-2xl">
              <NuxtImg src="/foto-profil.jpeg"
                class="w-full h-full object-cover transition-transform duration-1000 group-hover:scale-110" />
              <div
                class="absolute bottom-0 left-0 right-0 p-8 bg-gradient-to-t from-[#030712] via-[#030712]/60 to-transparent text-center">
                <h4 class="text-2xl font-black text-white italic">Bimo Surya Anggara</h4>
                <p class="text-sm font-bold text-indigo-400 uppercase tracking-widest mt-1 italic">Data Enthusiast</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="profil" class="py-32 bg-[#020617]">
      <div class="container mx-auto px-6 max-w-5xl">

        <h3 class="text-4xl md:text-5xl font-black mb-16 text-center">
          <span class="text-blue-500">Profil</span> <span class="text-yellow-500">Diri</span>
        </h3>

        <div
          class="bg-gradient-to-br from-blue-900/20 via-[#030712] to-yellow-900/10 border border-white/10 rounded-[2rem] p-8 md:p-12 shadow-2xl backdrop-blur-md flex flex-col md:flex-row items-center md:items-start gap-10 hover:border-blue-500/30 transition-colors duration-500">

          <div class="flex-shrink-0">
            <div
              class="w-48 h-48 md:w-56 md:h-56 rounded-full border-4 border-blue-500 p-1.5 relative group shadow-[0_0_30px_rgba(59,130,246,0.3)]">
              <div class="w-full h-full rounded-full overflow-hidden bg-white/5">
                <NuxtImg src="/foto-profil.jpeg" alt="Foto Bimo"
                  class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              </div>
            </div>
          </div>

          <div class="flex-grow text-center md:text-left">
            <h4 class="text-3xl md:text-4xl font-black text-blue-500 mb-6">Bimo Surya Anggara</h4>

            <div class="space-y-4 text-slate-300 leading-relaxed text-sm md:text-base">
              <p>
                Halo! Saya adalah seorang mahasiswa di program studi D4 Teknik Informatika Politeknik Negeri Bandung
                (POLBAN). Saya memiliki minat yang besar dalam dunia teknologi, khususnya dalam bidang <span
                  class="text-white font-bold">Software Engineering</span> dan <span class="text-white font-bold">Data
                  Analytics</span>.
              </p>
              <p>
                Saya percaya dengan kemampuan saya untuk menghadapi tantangan dan mengambil keputusan dengan tepat.
                <span class="text-yellow-400 font-bold italic">Saya orang yang bertanggung jawab, mudah diandalkan, dan
                  selalu berusaha memberikan yang terbaik dalam setiap kesempatan.</span>, Tujuan saya adalah terus
                berkembang, memberikan kontribusi nyata, dan meninggalkan dampak positif di lingkungan sekitar.
              </p>
            </div>

            <div class="mt-8 flex flex-wrap justify-center md:justify-start gap-3">
              <span
                class="px-5 py-2 bg-blue-500/10 border border-blue-500/20 rounded-full text-blue-400 text-xs font-bold tracking-wider uppercase">Mahasiswa
                POLBAN</span>
              <span
                class="px-5 py-2 bg-yellow-500/10 border border-yellow-500/20 rounded-full text-yellow-500 text-xs font-bold tracking-wider uppercase">Bandung,
                ID</span>
            </div>
          </div>

        </div>

      </div>
    </section>

    <section id="skill" class="py-32 bg-[#030712]">
      <div class="container mx-auto px-6 text-center">
        <h3 class="text-4xl font-black mb-20 italic">TECHNICAL <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-indigo-500">EXPERTISE</span></h3>
        <div class="space-y-24 text-left">
          <div v-for="category in skillCategories" :key="category.title">
            <h4 class="text-xs font-black mb-10 text-slate-600 uppercase tracking-[0.4em] flex items-center gap-6">
              {{ category.title }} <span class="h-px bg-white/5 flex-grow"></span>
            </h4>
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
              <div v-for="skill in category.skills" :key="skill.name"
                class="group bg-white/[0.03] p-8 rounded-3xl border border-white/5 hover:border-blue-500/50 transition-all duration-500">
                <Icon :name="skill.icon" class="text-5xl mb-6 grayscale group-hover:grayscale-0 transition-all" />
                <p class="font-black text-sm text-slate-500 group-hover:text-white uppercase tracking-widest">{{
                  skill.name }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="penugasan" class="py-32 bg-[#020617]">
      <div class="container mx-auto px-6 max-w-4xl">
        <h3
          class="text-4xl md:text-5xl font-black mb-16 uppercase text-center text-transparent bg-clip-text bg-gradient-to-r from-yellow-400 to-yellow-600">
          Penugasan
        </h3>

        <div class="space-y-12">

          <div
            class="bg-blue-950/30 border border-blue-500/20 rounded-2xl p-6 md:p-8 relative overflow-hidden group hover:border-blue-500/50 transition-colors">
            <div class="absolute top-0 left-0 w-2 h-full bg-blue-600"></div>

            <div class="flex flex-col md:flex-row gap-6 items-start">
              <div class="bg-blue-600 text-white p-4 rounded-xl shadow-lg shadow-blue-600/20 flex-shrink-0">
                <Icon name="mdi:file-document" class="text-3xl" />
              </div>

              <div class="flex-grow">
                <h4 class="text-2xl font-black text-white mb-3">Penugasan 2 - Dokumen</h4>
                <p class="text-slate-400 text-sm md:text-base leading-relaxed mb-6">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et
                  dolore magna aliqua.
                </p>

                <div class="flex flex-wrap gap-4">
                  <a href="https://docs.google.com/document/d/1b4DjzDShJCfE_U_Cea8Irtc7raNc9YM_/edit?usp=sharing&ouid=112043979209706907752&rtpof=true&sd=true"
                    target="_blank"
                    class="inline-flex items-center gap-2 bg-yellow-500 hover:bg-yellow-400 text-yellow-950 font-bold py-2.5 px-6 rounded-lg transition-all text-sm">
                    <Icon name="mdi:file-document-outline" class="text-lg" /> LIHAT HASIL TUGAS
                  </a>

                  <a href="/dokumen-tor.pdf" target="_blank"
                    class="inline-flex items-center gap-2 bg-blue-600 hover:bg-blue-500 text-white font-bold py-2.5 px-6 rounded-lg transition-all text-sm">
                    <Icon name="mdi:link-variant" class="text-lg" /> CONTOH DOKUMEN TOR
                  </a>
                </div>
              </div>
            </div>
          </div>

          <div
            class="bg-yellow-950/20 border border-yellow-500/20 rounded-2xl p-6 md:p-8 relative overflow-hidden group hover:border-yellow-500/50 transition-colors">
            <div class="absolute top-0 left-0 w-2 h-full bg-yellow-500"></div>

            <div class="flex flex-col md:flex-row gap-6 items-start mb-8">
              <div class="bg-yellow-500 text-yellow-950 p-4 rounded-xl shadow-lg shadow-yellow-500/20 flex-shrink-0">
                <Icon name="mdi:image-outline" class="text-3xl" />
              </div>

              <div>
                <h4 class="text-2xl font-black text-white mb-3">Penugasan 3 - Infografis</h4>
                <p class="text-slate-400 text-sm md:text-base leading-relaxed">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et
                  dolore magna aliqua.
                </p>
              </div>
            </div>

            <div class="bg-[#030712] p-4 rounded-xl border border-white/5 shadow-inner mb-8">
              <NuxtImg src="/infografis-bimo.png" alt="Poster Penugasan"
                class="w-full h-auto rounded-lg border border-white/10" />
            </div>

            <div class="flex justify-center">
              <a href="/infografis-bimo.png" download
                class="inline-flex items-center gap-2 bg-yellow-500 hover:bg-yellow-400 hover:scale-105 text-yellow-950 font-black py-3 px-8 rounded-full transition-all text-sm shadow-lg shadow-yellow-500/20">
                <Icon name="mdi:download" class="text-xl" /> Download Infografis
              </a>
            </div>
          </div>

          <div
            class="bg-indigo-950/20 border border-indigo-500/20 rounded-2xl p-6 md:p-8 relative overflow-hidden group hover:border-indigo-500/50 transition-colors">
            <div class="absolute top-0 left-0 w-2 h-full bg-indigo-500"></div>

            <div class="flex flex-col md:flex-row gap-6 items-start mb-8">
              <div class="bg-indigo-600 text-white p-4 rounded-xl shadow-lg shadow-indigo-600/20 flex-shrink-0">
                <Icon name="mdi:video-outline" class="text-3xl" />
              </div>

              <div>
                <h4 class="text-2xl font-black text-white mb-3">Penugasan 4 - Video</h4>
                <p class="text-slate-400 text-sm md:text-base leading-relaxed">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et
                  dolore magna aliqua.
                </p>
              </div>
            </div>

            <div class="bg-[#030712] p-4 rounded-xl border border-white/5 shadow-inner">
              <video controls class="w-full h-auto rounded-lg border border-white/10 outline-none shadow-2xl">
                <source src="">
                Maaf, browser Anda tidak mendukung pemutaran video ini.
              </video>
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="portofolio" class="py-32 bg-[#030712]">
      <div class="container mx-auto px-6 text-center md:text-left">
        <h3 class="text-4xl font-black mb-16 italic tracking-tight uppercase">
          My <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-indigo-500 text-white">Certificates</span>
        </h3>

        <div class="grid md:grid-cols-2 gap-10 mb-20">
          <div v-for="cert in certificates" :key="cert.title"
            class="bg-white/[0.02] p-8 rounded-[2rem] border border-white/10 hover:border-blue-500/30 transition-all group">
            <div
              class="w-full aspect-video bg-white/5 rounded-2xl overflow-hidden mb-6 border border-white/5 relative flex items-center justify-center group-hover:border-blue-500/30 transition-all">
              <NuxtImg :src="cert.image"
                class="min-w-full min-h-full object-cover -rotate-90 scale-[0.6] grayscale group-hover:grayscale-0 transition-all duration-700" />
            </div>
            <h4 class="text-2xl font-black mb-2 italic text-white/90">{{ cert.title }}</h4>
            <p class="text-[10px] font-black text-blue-400 uppercase tracking-widest mb-4 italic">{{ cert.issuer }} • {{
              cert.date }}</p>
            <p class="text-slate-500 text-sm leading-relaxed italic">{{ cert.description }}</p>
          </div>
        </div>

        <div
          class="bg-gradient-to-br from-blue-600/10 via-transparent to-indigo-600/10 p-12 rounded-[3rem] border border-white/5 relative overflow-hidden">
          <h4 class="text-2xl font-black mb-2 italic text-white/90 uppercase">Personal Portfolio Website</h4>
          <p class="text-xs font-bold text-slate-500 uppercase tracking-[0.4em] mb-6 italic">Tech Stack: Nuxt.js &
            Tailwind CSS</p>
          <p class="text-slate-400 text-sm max-w-2xl leading-relaxed italic">Proyek representasi digital Informatika
            menggunakan teknologi modern.</p>
          <div class="absolute -right-20 -bottom-20 w-80 h-80 bg-blue-600/10 rounded-full blur-[100px]"></div>
        </div>
      </div>
    </section>

    <footer id="kontak" class="py-20 bg-[#020617] border-t border-white/5 relative overflow-hidden">
      <div
        class="absolute top-0 left-1/2 -translate-x-1/2 w-full max-w-4xl h-1/2 bg-blue-600/10 blur-[120px] rounded-full pointer-events-none">
      </div>

      <div class="container mx-auto px-6 relative z-10">

        <div class="text-center mb-16">
          <h3 class="text-4xl md:text-5xl font-black mb-4">
            <span class="text-yellow-500">Kontak</span> <span class="text-white">Saya</span>
          </h3>
          <p class="text-slate-400 text-sm md:text-base max-w-2xl mx-auto">
            Contact me via the following social media.
          </p>
        </div>

        <div class="flex flex-wrap justify-center gap-6 md:gap-8 mb-16">

          <a href="https://github.com/Bisura16" target="_blank"
            class="group flex flex-col items-center justify-center w-36 h-36 md:w-44 md:h-44 bg-white rounded-3xl shadow-xl hover:-translate-y-2 hover:shadow-2xl hover:shadow-slate-500/20 transition-all duration-300">
            <div class="text-slate-800 group-hover:text-black transition-colors mb-3">
              <Icon name="mdi:github" class="text-5xl md:text-6xl" />
            </div>
            <h4 class="text-slate-900 font-black text-lg">GitHub</h4>
            <p class="text-slate-500 text-xs mt-1 font-medium">@Bisura16</p>
          </a>

          <a href="https://www.instagram.com/suryangraa" target="_blank"
            class="group flex flex-col items-center justify-center w-36 h-36 md:w-44 md:h-44 bg-white rounded-3xl shadow-xl hover:-translate-y-2 hover:shadow-2xl hover:shadow-pink-500/20 transition-all duration-300">
            <div class="text-pink-600 group-hover:text-pink-500 transition-colors mb-3">
              <Icon name="mdi:instagram" class="text-5xl md:text-6xl" />
            </div>
            <h4 class="text-slate-900 font-black text-lg">Instagram</h4>
            <p class="text-slate-500 text-xs mt-1 font-medium">@suryangraa</p>
          </a>

          <a href="https://wa.me/6281234567890" target="_blank"
            class="group flex flex-col items-center justify-center w-36 h-36 md:w-44 md:h-44 bg-white rounded-3xl shadow-xl hover:-translate-y-2 hover:shadow-2xl hover:shadow-green-500/20 transition-all duration-300">
            <div class="text-green-500 group-hover:text-green-400 transition-colors mb-3">
              <Icon name="mdi:whatsapp" class="text-5xl md:text-6xl" />
            </div>
            <h4 class="text-slate-900 font-black text-lg">WhatsApp</h4>
            <p class="text-slate-500 text-xs mt-1 font-medium">+62 819-3263-4786</p>
          </a>

          <a href="https://www.linkedin.com/in/bimo-surya-anggara" target="_blank"
            class="group flex flex-col items-center justify-center w-36 h-36 md:w-44 md:h-44 bg-white rounded-3xl shadow-xl hover:-translate-y-2 hover:shadow-2xl hover:shadow-blue-500/20 transition-all duration-300">
            <div class="text-blue-600 group-hover:text-blue-500 transition-colors mb-3">
              <Icon name="mdi:linkedin" class="text-5xl md:text-6xl" />
            </div>
            <h4 class="text-slate-900 font-black text-lg">LinkedIn</h4>
            <p class="text-slate-500 text-xs mt-1 font-medium">Bimo Surya A.</p>
          </a>

        </div>

        <div
          class="max-w-3xl mx-auto bg-blue-900/20 border border-blue-500/20 rounded-3xl p-8 md:p-10 text-center backdrop-blur-sm mb-12">
          <h4 class="text-lg md:text-xl font-bold text-slate-300 mb-3">
            Email: <a href="mailto:anggarabimo16@gmail.com"
              class="text-yellow-400 hover:text-yellow-300 transition-colors">anggarabimo16@gmail.com</a>
          </h4>
          <p class="text-slate-400 text-sm leading-relaxed max-w-xl mx-auto">
            Itulah sekilas tentang perjalanan dan karya saya. Saya selalu terbuka untuk tantangan baru, kolaborasi, dan
            kesempatan untuk membuat hal-hal hebat bersama. Mari kita ciptakan sesuatu yang luar biasa!
          </p>
        </div>

      </div>

      <div class="w-full bg-[#010409] py-6 text-center border-t border-white/5">
        <p class="text-[10px] md:text-xs font-bold text-slate-600 uppercase tracking-widest">
          &copy; 2026 BIMO SURYA ANGGARA • TEKNIK INFORMATIKA POLBAN
        </p>
      </div>
    </footer>
  </div>
</template>

<style>
::selection {
  background-color: rgba(99, 102, 241, 0.3);
  color: white;
}

html {
  scroll-behavior: smooth;
  background-color: #030712;
}

body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
}
</style>