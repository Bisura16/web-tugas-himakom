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
          <a href="#kontak" class="bg-gradient-to-r from-blue-600 to-indigo-600 text-white px-5 py-2 rounded-full hover:scale-105 transition-transform shadow-lg shadow-indigo-500/20">Kontak</a>
        </div>
      </div>
    </nav>

    <section id="beranda" class="min-h-[95vh] flex items-center relative overflow-hidden py-20">
      <div class="absolute top-0 left-0 w-[600px] h-[600px] bg-blue-600/20 rounded-full blur-[140px] -translate-x-1/2 -translate-y-1/2"></div>
      <div class="absolute bottom-0 right-0 w-[600px] h-[600px] bg-indigo-600/20 rounded-full blur-[140px] translate-x-1/2 translate-y-1/2"></div>
      <div class="container mx-auto px-6 z-10 flex flex-col md:flex-row items-center gap-16">
        <div class="md:w-3/5">
          <div class="inline-flex items-center gap-2 bg-white/5 border border-white/10 px-4 py-1.5 rounded-full mb-6">
            <span class="w-2 h-2 bg-blue-500 rounded-full animate-ping"></span>
            <span class="text-xs font-bold tracking-widest text-slate-300 uppercase">Available for Projects</span>
          </div>
          <h2 class="text-6xl md:text-8xl font-black mb-6 leading-[1.1] tracking-tight">
            Bimo Surya <br>
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 via-indigo-400 to-purple-500">Anggara</span>
          </h2>
          <p class="text-xl md:text-2xl font-medium text-slate-400 mb-10 leading-relaxed max-w-xl">
            Software Engineer & Data Enthusiast. <span class="text-white font-bold">Mahasiswa D4 Teknik Informatika POLBAN.</span>
          </p>
          <div class="flex gap-6 mb-12">
            <a v-for="link in socialLinks" :key="link.name" :href="link.url" target="_blank"
               class="text-2xl text-slate-500 hover:text-blue-400 hover:-translate-y-1 transition-all">
              <Icon :name="link.icon" />
            </a>
          </div>
          <div class="flex flex-wrap gap-5">
            <a href="#penugasan" class="group bg-white text-black px-10 py-4 rounded-full font-black hover:bg-gradient-to-r from-blue-500 to-indigo-600 hover:text-white transition-all duration-300 flex items-center gap-2 shadow-xl shadow-white/5">
              Lihat Karya <Icon name="material-symbols:arrow-right-alt" class="group-hover:translate-x-2 transition-transform" />
            </a>
            <a href="#kontak" class="border border-white/10 bg-white/5 backdrop-blur-md px-10 py-4 rounded-full font-black hover:bg-white/10 transition-all">Kontak Saya</a>
          </div>
        </div>
        <div class="md:w-2/5 flex justify-center">
          <div class="relative group p-4 bg-white/5 border border-white/10 rounded-[2.5rem] backdrop-blur-2xl">
            <div class="w-72 h-[450px] md:w-80 md:h-[520px] rounded-[2rem] overflow-hidden relative shadow-2xl">
              <NuxtImg src="/foto-profil.jpeg" class="w-full h-full object-cover transition-transform duration-1000 group-hover:scale-110" />
              <div class="absolute bottom-0 left-0 right-0 p-8 bg-gradient-to-t from-[#030712] via-[#030712]/60 to-transparent text-center">
                <h4 class="text-2xl font-black text-white italic">Bimo Surya Anggara</h4>
                <p class="text-sm font-bold text-indigo-400 uppercase tracking-widest mt-1 italic">Data Enthusiast</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="profil" class="py-32 bg-[#020617]">
      <div class="container mx-auto px-6">
        <h3 class="text-sm font-black text-blue-500 uppercase tracking-[0.5em] mb-12">PROFIL DIRI</h3>
        <div class="grid md:grid-cols-2 gap-20 items-center">
          <div class="relative group">
            <div class="absolute -inset-1 bg-gradient-to-r from-blue-600 to-indigo-600 rounded-3xl blur opacity-25 group-hover:opacity-50 transition duration-1000"></div>
            <div class="relative bg-[#030712] h-[400px] w-full rounded-3xl border border-white/5 flex items-center justify-center overflow-hidden">
               <span class="text-white font-black text-[120px] opacity-[0.03] select-none">POLBAN</span>
               <div class="text-center z-10">
                 <p class="text-5xl font-black italic text-transparent bg-clip-text bg-gradient-to-b from-white to-white/20">D4 TI</p>
               </div>
            </div>
          </div>
          <div>
            <h4 class="text-4xl font-black mb-6">Membangun Masa Depan <br> Lewat <span class="text-blue-500 italic">Kode & Data.</span></h4>
            <p class="text-xl leading-relaxed text-slate-400 mb-10">
              Sebagai mahasiswa <span class="text-white font-bold">Teknik Informatika POLBAN</span>, saya fokus pada efisiensi algoritma dan performa sistem.
            </p>
            <div class="flex gap-6">
              <div class="bg-white/5 p-6 rounded-2xl border border-white/10 flex-1 text-center font-black">
                <p class="text-[10px] text-slate-500 uppercase mb-2">MBTI</p>
                <p class="text-2xl text-blue-400 italic">ENTJ</p>
              </div>
              <div class="bg-white/5 p-6 rounded-2xl border border-white/10 flex-1 text-center font-black">
                <p class="text-[10px] text-slate-500 uppercase mb-2">Location</p>
                <p class="text-2xl text-indigo-400 italic">Bandung</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="skill" class="py-32 bg-[#030712]">
      <div class="container mx-auto px-6 text-center">
        <h3 class="text-4xl font-black mb-20 italic">TECHNICAL <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-indigo-500">EXPERTISE</span></h3>
        <div class="space-y-24 text-left">
          <div v-for="category in skillCategories" :key="category.title">
            <h4 class="text-xs font-black mb-10 text-slate-600 uppercase tracking-[0.4em] flex items-center gap-6">
              {{ category.title }} <span class="h-px bg-white/5 flex-grow"></span>
            </h4>
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
              <div v-for="skill in category.skills" :key="skill.name" 
                   class="group bg-white/[0.03] p-8 rounded-3xl border border-white/5 hover:border-blue-500/50 transition-all duration-500">
                <Icon :name="skill.icon" class="text-5xl mb-6 grayscale group-hover:grayscale-0 transition-all" />
                <p class="font-black text-sm text-slate-500 group-hover:text-white uppercase tracking-widest">{{ skill.name }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="penugasan" class="py-32 bg-[#020617]">
      <div class="container mx-auto px-6">
        <h3 class="text-5xl font-black italic mb-16 uppercase">Dokumentasi <span class="text-blue-600">Penugasan</span></h3>
        <div class="grid md:grid-cols-3 gap-8">
          <div v-for="n in [2, 3, 4]" :key="n" class="relative group p-10 bg-[#030712] rounded-3xl border border-white/5 hover:border-white/20 transition-all">
            <p class="text-6xl font-black text-white/5 absolute top-6 right-8">0{{ n }}</p>
            <h4 class="text-2xl font-black mb-4 italic">Penugasan {{ n }}</h4>
            <p class="text-slate-500 text-sm leading-relaxed mb-8 italic">Implementasi proyek mata kuliah Informatika POLBAN.</p>
            <div class="h-1 w-12 bg-blue-600 group-hover:w-full transition-all duration-500 rounded-full"></div>
          </div>
        </div>
      </div>
    </section>

    <section id="portofolio" class="py-32 bg-[#030712]">
      <div class="container mx-auto px-6 text-center md:text-left">
        <h3 class="text-4xl font-black mb-16 italic tracking-tight uppercase">
          My <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-indigo-500 text-white">Certificates</span>
        </h3>
        
        <div class="grid md:grid-cols-2 gap-10 mb-20">
          <div v-for="cert in certificates" :key="cert.title" 
               class="bg-white/[0.02] p-8 rounded-[2rem] border border-white/10 hover:border-blue-500/30 transition-all group">
<div class="w-full aspect-video bg-white/5 rounded-2xl overflow-hidden mb-6 border border-white/5 relative flex items-center justify-center group-hover:border-blue-500/30 transition-all">
  <NuxtImg 
    :src="cert.image" 
    class="min-w-full min-h-full object-cover -rotate-90 scale-[0.6] grayscale group-hover:grayscale-0 transition-all duration-700" 
  />
</div>
            <h4 class="text-2xl font-black mb-2 italic text-white/90">{{ cert.title }}</h4>
            <p class="text-[10px] font-black text-blue-400 uppercase tracking-widest mb-4 italic">{{ cert.issuer }} • {{ cert.date }}</p>
            <p class="text-slate-500 text-sm leading-relaxed italic">{{ cert.description }}</p>
          </div>
        </div>

        <div class="bg-gradient-to-br from-blue-600/10 via-transparent to-indigo-600/10 p-12 rounded-[3rem] border border-white/5 relative overflow-hidden">
          <h4 class="text-2xl font-black mb-2 italic text-white/90 uppercase">Personal Portfolio Website</h4>
          <p class="text-xs font-bold text-slate-500 uppercase tracking-[0.4em] mb-6 italic">Tech Stack: Nuxt.js & Tailwind CSS</p>
          <p class="text-slate-400 text-sm max-w-2xl leading-relaxed italic">Proyek representasi digital Informatika menggunakan teknologi modern.</p>
          <div class="absolute -right-20 -bottom-20 w-80 h-80 bg-blue-600/10 rounded-full blur-[100px]"></div>
        </div>
      </div>
    </section>

    <footer id="kontak" class="py-32 bg-[#030712] border-t border-white/5 text-center">
      <div class="container mx-auto px-6">
        <h3 class="text-6xl md:text-8xl font-black mb-12 italic tracking-tighter uppercase">Say <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-indigo-500 to-purple-600">Hello.</span></h3>
        <div class="flex flex-wrap justify-center gap-6 mb-24">
          <a href="mailto:bimo@polban.ac.id" class="bg-white text-black px-12 py-5 rounded-full font-black text-lg hover:bg-blue-600 hover:text-white transition-all shadow-2xl">Email Me</a>
          <a href="https://github.com/Bisura16" target="_blank" class="border-2 border-white/10 px-12 py-5 rounded-full font-black text-lg hover:bg-white hover:text-black transition-all shadow-xl">GitHub</a>
        </div>
        <p class="text-[10px] font-black text-slate-700 uppercase tracking-[0.5em] italic">&copy; 2026 BIMO SURYA ANGGARA • TEKNIK INFORMATIKA POLBAN</p>
      </div>
    </footer>
  </div>
</template>

<style>
::selection { background-color: rgba(99, 102, 241, 0.3); color: white; }
html { scroll-behavior: smooth; background-color: #030712; }
body { font-family: 'Plus Jakarta Sans', sans-serif; -webkit-font-smoothing: antialiased; }
</style>