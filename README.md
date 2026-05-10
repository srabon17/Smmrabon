<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Srabon Chandra Das — Digital Marketer & Graphic Designer</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://code.iconify.design/3/3.1.0/iconify.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            celadon: '#9cdcaa',
            darkSurface: '#2b2b2b',
            lightNeutral: '#f3f1ee',
            bgBlack: '#0b0b0b',
          },
          fontFamily: {
            poppins: ['Poppins', 'sans-serif'],
          }
        }
      }
    }
  </script>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body { font-family: 'Poppins', sans-serif; background: #0b0b0b; color: #f3f1ee; overflow-x: hidden; }
    ::selection { background: #9cdcaa; color: #0b0b0b; }
    ::-webkit-scrollbar { width: 8px; }
    ::-webkit-scrollbar-track { background: #0b0b0b; }
    ::-webkit-scrollbar-thumb { background: #9cdcaa33; border-radius: 4px; }
    ::-webkit-scrollbar-thumb:hover { background: #9cdcaa66; }

    @keyframes fadeSlideIn {
      0% { opacity: 0; transform: translateY(30px); filter: blur(8px); }
      100% { opacity: 1; transform: translateY(0); filter: blur(0); }
    }
    .anim-in { animation: fadeSlideIn 0.8s ease-out both; }
    .anim-d1 { animation-delay: 0s; }
    .anim-d2 { animation-delay: 0.2s; }
    .anim-d3 { animation-delay: 0.4s; }
    .anim-d4 { animation-delay: 0.6s; }
    .anim-d5 { animation-delay: 0.8s; }
    .anim-d6 { animation-delay: 1s; }

    @keyframes blob {
      0% { transform: translate(0,0) scale(1); }
      33% { transform: translate(30px,-50px) scale(1.1); }
      66% { transform: translate(-20px,20px) scale(0.9); }
      100% { transform: translate(0,0) scale(1); }
    }
    .blob { animation: blob 10s infinite cubic-bezier(0.4,0,0.2,1); mix-blend-mode: screen; }
    .blob-1 { animation-delay: 0s; }
    .blob-2 { animation-delay: 2s; }
    .blob-3 { animation-delay: 4s; }

    @keyframes beam-drop {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(100%); }
    }
    @keyframes beam-slide {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
    }
    .float-anim { animation: float 6s ease-in-out infinite; }
    .float-anim-d1 { animation-delay: 0s; }
    .float-anim-d2 { animation-delay: 1.5s; }
    .float-anim-d3 { animation-delay: 3s; }

    @keyframes pulse-ring {
      0% { transform: scale(1); opacity: 0.6; }
      100% { transform: scale(1.8); opacity: 0; }
    }

    @keyframes counter {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .scroll-reveal {
      opacity: 0;
      transform: translateY(40px);
      filter: blur(6px);
      transition: all 0.8s ease-out;
    }
    .scroll-reveal.revealed {
      opacity: 1;
      transform: translateY(0);
      filter: blur(0);
    }

    .card-hover {
      transition: all 0.5s cubic-bezier(0.25,0.46,0.45,0.94);
    }
    .card-hover:hover {
      transform: translateY(-10px) scale(1.02);
      box-shadow: 0 25px 50px -12px rgba(0,0,0,0.5);
      border-color: rgba(156,220,170,0.3);
    }

    .skill-tag {
      transition: all 0.3s ease;
    }
    .skill-tag:hover {
      background: #9cdcaa;
      color: #0b0b0b;
      transform: translateY(-2px);
    }

    .nav-link {
      position: relative;
    }
    .nav-link::after {
      content: '';
      position: absolute;
      bottom: -4px;
      left: 0;
      width: 0;
      height: 2px;
      background: #9cdcaa;
      transition: width 0.3s ease;
    }
    .nav-link:hover::after {
      width: 100%;
    }

    .portfolio-item .overlay {
      opacity: 0;
      transition: all 0.5s ease;
    }
    .portfolio-item:hover .overlay {
      opacity: 1;
    }
    .portfolio-item:hover .portfolio-img {
      transform: scale(1.08);
    }
    .portfolio-img {
      transition: transform 0.7s ease;
    }

    .magnetic-btn {
      transition: all 0.3s ease;
    }
    .magnetic-btn:hover {
      background: #9cdcaa;
      color: #0b0b0b;
      box-shadow: 0 0 40px rgba(156,220,170,0.3);
    }

    .toast {
      position: fixed;
      bottom: 30px;
      right: 30px;
      background: #2b2b2b;
      border: 1px solid rgba(156,220,170,0.3);
      color: #f3f1ee;
      padding: 16px 24px;
      border-radius: 12px;
      z-index: 1000;
      transform: translateY(100px);
      opacity: 0;
      transition: all 0.4s ease;
    }
    .toast.show {
      transform: translateY(0);
      opacity: 1;
    }

    .mobile-menu {
      transform: translateX(100%);
      transition: transform 0.4s cubic-bezier(0.25,0.46,0.45,0.94);
    }
    .mobile-menu.open {
      transform: translateX(0);
    }

    .timeline-line {
      background: linear-gradient(to bottom, transparent, #9cdcaa, transparent);
    }
  </style>
</head>
<body>

  <!-- ========== NAVIGATION ========== -->
  <nav id="navbar" class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 py-6 lg:py-8 px-6 lg:px-12">
    <div class="max-w-[90rem] mx-auto flex items-center justify-between">
      <a href="#hero" class="text-xl font-bold tracking-tight text-lightNeutral">
        <span class="text-celadon">S</span>rabon<span class="text-celadon">.</span>
      </a>
      <div class="hidden md:flex items-center gap-8">
        <a href="#about" class="nav-link text-sm font-light text-lightNeutral/70 hover:text-celadon transition-colors duration-300">About</a>
        <a href="#skills" class="nav-link text-sm font-light text-lightNeutral/70 hover:text-celadon transition-colors duration-300">Skills</a>
        <a href="#services" class="nav-link text-sm font-light text-lightNeutral/70 hover:text-celadon transition-colors duration-300">Services</a>
        <a href="#experience" class="nav-link text-sm font-light text-lightNeutral/70 hover:text-celadon transition-colors duration-300">Experience</a>
        <a href="#portfolio" class="nav-link text-sm font-light text-lightNeutral/70 hover:text-celadon transition-colors duration-300">Portfolio</a>
        <a href="#contact" class="magnetic-btn text-xs font-semibold uppercase tracking-wider border border-celadon/40 text-celadon px-5 py-2.5 rounded-full">
          Let's Talk
        </a>
      </div>
      <button id="menuBtn" class="md:hidden text-lightNeutral" onclick="toggleMenu()">
        <span class="iconify" data-icon="mdi:menu" data-width="28"></span>
      </button>
    </div>
  </nav>

  <!-- Mobile Menu -->
  <div id="mobileMenu" class="mobile-menu fixed top-0 right-0 w-72 h-full bg-bgBlack/95 backdrop-blur-xl z-50 border-l border-white/5 p-8 flex flex-col gap-6">
    <button onclick="toggleMenu()" class="self-end text-lightNeutral mb-4">
      <span class="iconify" data-icon="mdi:close" data-width="28"></span>
    </button>
    <a href="#about" onclick="toggleMenu()" class="text-lg font-light text-lightNeutral/70 hover:text-celadon transition-colors">About</a>
    <a href="#skills" onclick="toggleMenu()" class="text-lg font-light text-lightNeutral/70 hover:text-celadon transition-colors">Skills</a>
    <a href="#services" onclick="toggleMenu()" class="text-lg font-light text-lightNeutral/70 hover:text-celadon transition-colors">Services</a>
    <a href="#experience" onclick="toggleMenu()" class="text-lg font-light text-lightNeutral/70 hover:text-celadon transition-colors">Experience</a>
    <a href="#portfolio" onclick="toggleMenu()" class="text-lg font-light text-lightNeutral/70 hover:text-celadon transition-colors">Portfolio</a>
    <a href="#contact" onclick="toggleMenu()" class="magnetic-btn text-sm font-semibold uppercase tracking-wider border border-celadon/40 text-celadon px-5 py-2.5 rounded-full text-center mt-4">Let's Talk</a>
  </div>

  <!-- ========== HERO ========== -->
  <section id="hero" class="relative min-h-screen flex items-center overflow-hidden pt-32 lg:pt-40 pb-20 px-6 lg:px-12">
    <!-- Blobs -->
    <div class="absolute top-1/4 -left-20 w-72 h-72 bg-celadon/20 rounded-full blob blob-1" style="filter:blur(80px)"></div>
    <div class="absolute top-1/3 right-10 w-80 h-80 bg-purple-500/20 rounded-full blob blob-2" style="filter:blur(100px)"></div>
    <div class="absolute bottom-20 left-1/3 w-64 h-64 bg-blue-500/20 rounded-full blob blob-3" style="filter:blur(80px)"></div>

    <!-- Beams -->
    <div class="absolute top-0 left-1/4 w-px h-full overflow-hidden opacity-10">
      <div class="w-full h-1/3 bg-gradient-to-b from-transparent via-celadon to-transparent" style="animation:beam-drop 5s linear infinite"></div>
    </div>
    <div class="absolute top-1/2 left-0 h-px w-full overflow-hidden opacity-10">
      <div class="h-full w-1/3 bg-gradient-to-r from-transparent via-celadon to-transparent" style="animation:beam-slide 7s linear infinite; animation-delay:2.5s"></div>
    </div>

    <div class="max-w-[90rem] mx-auto w-full grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
      <!-- Left Content -->
      <div class="lg:col-span-5 flex flex-col justify-center">
        <div class="anim-in anim-d1 mb-4">
          <span class="inline-flex items-center gap-2 text-[10px] uppercase tracking-[0.25em] text-celadon font-medium border border-celadon/20 rounded-full px-4 py-1.5 backdrop-blur-sm bg-white/5">
            <span class="w-2 h-2 bg-celadon rounded-full relative">
              <span class="absolute inset-0 bg-celadon rounded-full" style="animation:pulse-ring 2s ease-out infinite"></span>
            </span>
            Available for Projects
          </span>
        </div>
        <h1 class="anim-in anim-d2 text-[clamp(2.2rem,6vw,4.5rem)] font-bold leading-[1.0] tracking-[-0.03em] uppercase mb-6">
          Srabon<br>
          <span class="text-celadon">Chandra</span><br>
          Das
        </h1>
        <p class="anim-in anim-d3 text-base lg:text-lg font-light text-lightNeutral/60 leading-relaxed max-w-md mb-8">
          Crafting visual stories & driving digital growth — where <span class="text-celadon font-normal">creative design</span> meets <span class="text-celadon font-normal">strategic marketing</span>.
        </p>
        <div class="anim-in anim-d4 flex flex-wrap gap-4">
          <a href="#portfolio" class="magnetic-btn inline-flex items-center gap-2 text-sm font-semibold uppercase tracking-wider border border-celadon text-celadon px-7 py-3.5 rounded-full">
            View My Work
            <span class="iconify" data-icon="mdi:arrow-right" data-width="18"></span>
          </a>
          <a href="#contact" class="inline-flex items-center gap-2 text-sm font-semibold uppercase tracking-wider text-lightNeutral/70 hover:text-celadon px-4 py-3.5 transition-colors duration-300">
            Get in Touch
          </a>
        </div>
      </div>

      <!-- Center Visual -->
      <div class="lg:col-span-5 relative flex items-center justify-center min-h-[400px] lg:min-h-[500px]" style="perspective:1000px">
        <div class="relative w-64 h-80 lg:w-72 lg:h-96 rounded-2xl overflow-hidden border border-white/10 shadow-2xl float-anim float-anim-d1">
          <img src="https://picsum.photos/seed/srabon-portrait/400/550.jpg" alt="Srabon Chandra Das" class="w-full h-full object-cover">
          <div class="absolute inset-0 bg-gradient-to-t from-bgBlack via-transparent to-transparent"></div>
        </div>
        <!-- Floating cards -->
        <div class="absolute -top-4 -right-4 lg:right-0 bg-darkSurface/90 backdrop-blur-md border border-white/10 rounded-xl p-3 shadow-xl float-anim float-anim-d2">
          <div class="flex items-center gap-2">
            <span class="iconify text-celadon" data-icon="mdi:palette-outline" data-width="20"></span>
            <span class="text-xs font-medium text-lightNeutral">Designer</span>
          </div>
        </div>
        <div class="absolute -bottom-2 -left-4 lg:left-0 bg-darkSurface/90 backdrop-blur-md border border-white/10 rounded-xl p-3 shadow-xl float-anim float-anim-d3">
          <div class="flex items-center gap-2">
            <span class="iconify text-celadon" data-icon="mdi:trending-up" data-width="20"></span>
            <span class="text-xs font-medium text-lightNeutral">Marketer</span>
          </div>
        </div>
        <div class="absolute top-1/2 -right-8 lg:-right-12 bg-darkSurface/90 backdrop-blur-md border border-white/10 rounded-xl p-3 shadow-xl float-anim float-anim-d1">
          <div class="flex items-center gap-2">
            <span class="iconify text-celadon" data-icon="mdi:check-decagram" data-width="20"></span>
            <span class="text-xs font-medium text-lightNeutral">100+ Projects</span>
          </div>
        </div>
        <!-- Decorative ring -->
        <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
          <div class="w-80 h-80 lg:w-96 lg:h-96 rounded-full border border-celadon/10" style="animation:spin 20s linear infinite"></div>
        </div>
      </div>

      <!-- Right Stats -->
      <div class="lg:col-span-2 lg:border-l lg:border-white/5 lg:pl-8 flex lg:flex-col gap-8 lg:gap-12 justify-center">
        <div class="anim-in anim-d4">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-lightNeutral counter-num" data-target="100">0</div>
          <div class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/50 mt-1">Projects Done</div>
        </div>
        <div class="anim-in anim-d5">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-lightNeutral counter-num" data-target="5">0</div>
          <div class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/50 mt-1">Countries</div>
        </div>
        <div class="anim-in anim-d6">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-lightNeutral counter-num" data-target="3">0</div>
          <div class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/50 mt-1">Companies</div>
        </div>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 anim-in anim-d6">
      <span class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/30">Scroll</span>
      <div class="w-px h-8 bg-gradient-to-b from-celadon/50 to-transparent"></div>
    </div>
  </section>

  <!-- ========== ABOUT ========== -->
  <section id="about" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="max-w-[80rem] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <div class="scroll-reveal">
          <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">About Me</span>
          <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight mb-6">
            Turning Ideas Into<br><span class="text-celadon">Visual Impact</span>
          </h2>
          <p class="text-base font-light text-lightNeutral/60 leading-relaxed mb-6">
            I'm Srabon Chandra Das — a multidisciplinary creative professional with a passion for blending aesthetics with strategy. With years of hands-on experience spanning both <strong class="text-lightNeutral font-normal">digital marketing</strong> and <strong class="text-lightNeutral font-normal">graphic design</strong>, I help brands stand out in crowded markets and connect with their audiences on a deeper level.
          </p>
          <p class="text-base font-light text-lightNeutral/60 leading-relaxed mb-6">
            From designing scroll-stopping YouTube thumbnails that drive clicks, to building cohesive brand identities that earn trust, to running data-driven campaigns that deliver measurable ROI — I bring a rare dual perspective that bridges the gap between <span class="text-celadon">creative vision</span> and <span class="text-celadon">marketing results</span>.
          </p>
          <p class="text-base font-light text-lightNeutral/60 leading-relaxed mb-8">
            Having collaborated with clients across the UK, USA, Canada, Bangladesh, and India, I understand diverse market dynamics and tailor every project to resonate with its target audience. Whether you're a startup looking for a bold identity or an established brand seeking a digital refresh — I'm here to make it happen.
          </p>
          <div class="flex flex-wrap gap-3">
            <a href="#contact" class="magnetic-btn inline-flex items-center gap-2 text-sm font-semibold uppercase tracking-wider border border-celadon text-celadon px-6 py-3 rounded-full">
              Work With Me
              <span class="iconify" data-icon="mdi:arrow-right" data-width="16"></span>
            </a>
            <a href="#portfolio" class="inline-flex items-center gap-2 text-sm font-medium text-lightNeutral/50 hover:text-celadon px-4 py-3 transition-colors duration-300">
              See My Work
            </a>
          </div>
        </div>
        <div class="scroll-reveal relative">
          <div class="relative rounded-2xl overflow-hidden border border-white/10">
            <img src="https://picsum.photos/seed/srabon-workspace/600/700.jpg" alt="Srabon at work" class="w-full h-[400px] lg:h-[550px] object-cover">
            <div class="absolute inset-0 bg-gradient-to-t from-bgBlack/80 via-transparent to-transparent"></div>
            <div class="absolute bottom-6 left-6 right-6">
              <div class="bg-darkSurface/80 backdrop-blur-md border border-white/10 rounded-xl p-4 flex items-center gap-4">
                <div class="w-12 h-12 bg-celadon/10 rounded-full flex items-center justify-center">
                  <span class="iconify text-celadon" data-icon="mdi:lightning-bolt" data-width="24"></span>
                </div>
                <div>
                  <div class="text-sm font-semibold text-lightNeutral">Design + Strategy</div>
                  <div class="text-xs text-lightNeutral/50">Where creativity meets conversion</div>
                </div>
              </div>
            </div>
          </div>
          <!-- Decorative element -->
          <div class="absolute -top-6 -right-6 w-24 h-24 border border-celadon/20 rounded-2xl -z-10"></div>
          <div class="absolute -bottom-6 -left-6 w-32 h-32 border border-celadon/10 rounded-2xl -z-10"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== SKILLS ========== -->
  <section id="skills" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="max-w-[80rem] mx-auto">
      <div class="text-center mb-16 scroll-reveal">
        <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">My Expertise</span>
        <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight">
          Skills & <span class="text-celadon">Tools</span>
        </h2>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        <!-- Graphic Design Skills -->
        <div class="scroll-reveal card-hover bg-darkSurface/50 border border-white/5 rounded-2xl p-8">
          <div class="flex items-center gap-4 mb-8">
            <div class="w-14 h-14 bg-celadon/10 rounded-xl flex items-center justify-center">
              <span class="iconify text-celadon" data-icon="mdi:palette-outline" data-width="28"></span>
            </div>
            <div>
              <h3 class="text-xl font-semibold">Graphic Design</h3>
              <p class="text-xs text-lightNeutral/50">Visual communication & brand aesthetics</p>
            </div>
          </div>
          <div class="flex flex-wrap gap-2.5">
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">YouTube Thumbnail</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Logo Design</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">T-shirt Design</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Brand Identity</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Social Media Design</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Banner & Poster</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Business Card</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Packaging Design</span>
          </div>
        </div>

        <!-- Digital Marketing Skills -->
        <div class="scroll-reveal card-hover bg-darkSurface/50 border border-white/5 rounded-2xl p-8">
          <div class="flex items-center gap-4 mb-8">
            <div class="w-14 h-14 bg-celadon/10 rounded-xl flex items-center justify-center">
              <span class="iconify text-celadon" data-icon="mdi:chart-line" data-width="28"></span>
            </div>
            <div>
              <h3 class="text-xl font-semibold">Digital Marketing</h3>
              <p class="text-xs text-lightNeutral/50">Growth strategy & campaign execution</p>
            </div>
          </div>
          <div class="flex flex-wrap gap-2.5">
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Social Media Marketing</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">SEO Optimization</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Content Strategy</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Facebook Ads</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Google Ads</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Email Marketing</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Brand Strategy</span>
            <span class="skill-tag text-sm font-light text-lightNeutral/70 border border-white/10 rounded-full px-4 py-2 cursor-default">Analytics & Reporting</span>
          </div>
        </div>
      </div>

      <!-- Tools -->
      <div class="mt-12 scroll-reveal">
        <p class="text-center text-xs uppercase tracking-[0.2em] text-lightNeutral/30 mb-8">Tools I Work With</p>
        <div class="flex flex-wrap justify-center gap-6">
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:adobe" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Adobe Suite</span>
          </div>
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:google" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Google Ads</span>
          </div>
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:facebook" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Meta Ads</span>
          </div>
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:chart-box-outline" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Analytics</span>
          </div>
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:pencil-ruler" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Figma</span>
          </div>
          <div class="group flex flex-col items-center gap-2 opacity-50 hover:opacity-100 transition-opacity duration-300">
            <span class="iconify text-lightNeutral group-hover:text-celadon transition-colors" data-icon="mdi:email-fast-outline" data-width="32"></span>
            <span class="text-[10px] text-lightNeutral/50">Mailchimp</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== SERVICES ========== -->
  <section id="services" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="max-w-[80rem] mx-auto">
      <div class="text-center mb-16 scroll-reveal">
        <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">What I Offer</span>
        <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight">
          Services <span class="text-celadon">Tailored</span> For You
        </h2>
        <p class="text-base font-light text-lightNeutral/50 mt-4 max-w-xl mx-auto">
          End-to-end creative and marketing solutions designed to elevate your brand and accelerate growth.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Service 1 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:youtube" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">YouTube Thumbnail Design</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              Click-worthy thumbnails that boost CTR and make your videos impossible to scroll past. Designed for maximum visual impact.
            </p>
          </div>
        </div>

        <!-- Service 2 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:star-four-points-outline" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">Logo & Brand Identity</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              Memorable logos and cohesive brand systems that tell your story and create lasting recognition across every touchpoint.
            </p>
          </div>
        </div>

        <!-- Service 3 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:instagram" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">Social Media Design</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              Scroll-stopping visuals for Instagram, Facebook, LinkedIn & more — feed templates, stories, carousels, and ad creatives.
            </p>
          </div>
        </div>

        <!-- Service 4 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:tshirt-crew-outline" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">T-shirt & Merch Design</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              Trendy, print-ready apparel designs that people love to wear. From minimal typography to bold illustrations.
            </p>
          </div>
        </div>

        <!-- Service 5 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:bullhorn-outline" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">Social Media Marketing</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              Data-driven campaigns across Facebook, Instagram & Google. Strategy, execution, and optimization for real ROI.
            </p>
          </div>
        </div>

        <!-- Service 6 -->
        <div class="scroll-reveal card-hover group bg-darkSurface/50 border border-white/5 rounded-2xl p-8 relative overflow-hidden">
          <div class="absolute top-0 right-0 w-32 h-32 bg-celadon/5 rounded-full -translate-y-1/2 translate-x-1/2 group-hover:scale-150 transition-transform duration-700"></div>
          <div class="relative">
            <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center mb-6 group-hover:bg-celadon/20 transition-colors duration-300">
              <span class="iconify text-celadon" data-icon="mdi:rocket-launch-outline" data-width="24"></span>
            </div>
            <h3 class="text-lg font-semibold mb-3">Complete Brand Launch</h3>
            <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
              From zero to launch — logo, brand guidelines, marketing collateral, and digital strategy. Everything your new brand needs.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== EXPERIENCE ========== -->
  <section id="experience" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="absolute top-1/2 right-0 w-96 h-96 bg-celadon/10 rounded-full blob blob-2" style="filter:blur(120px)"></div>
    <div class="max-w-[80rem] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
        <div class="scroll-reveal">
          <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">Experience</span>
          <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight mb-6">
            Where I've <span class="text-celadon">Made Impact</span>
          </h2>
          <p class="text-base font-light text-lightNeutral/50 leading-relaxed">
            I've had the privilege of working with forward-thinking companies, helping them strengthen their brand presence and achieve measurable digital growth.
          </p>
        </div>

        <!-- Timeline -->
        <div class="relative scroll-reveal">
          <div class="absolute left-6 top-0 bottom-0 w-px timeline-line"></div>
          
          <!-- Company 1 -->
          <div class="relative pl-16 pb-12">
            <div class="absolute left-3.5 top-1 w-5 h-5 bg-celadon rounded-full border-4 border-bgBlack"></div>
            <div class="card-hover bg-darkSurface/50 border border-white/5 rounded-2xl p-6">
              <div class="flex items-center gap-3 mb-3">
                <div class="w-10 h-10 bg-celadon/10 rounded-lg flex items-center justify-center">
                  <span class="iconify text-celadon" data-icon="mdi:tech-icon" data-width="20"></span>
                </div>
                <div>
                  <h4 class="font-semibold text-lightNeutral">Arifin Tech</h4>
                  <span class="text-[10px] uppercase tracking-wider text-celadon">Digital Marketing & Design</span>
                </div>
              </div>
              <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
                Led visual branding and digital marketing campaigns, increasing social engagement by 40% and delivering cohesive brand assets across all channels.
              </p>
            </div>
          </div>

          <!-- Company 2 -->
          <div class="relative pl-16 pb-12">
            <div class="absolute left-3.5 top-1 w-5 h-5 bg-celadon rounded-full border-4 border-bgBlack"></div>
            <div class="card-hover bg-darkSurface/50 border border-white/5 rounded-2xl p-6">
              <div class="flex items-center gap-3 mb-3">
                <div class="w-10 h-10 bg-celadon/10 rounded-lg flex items-center justify-center">
                  <span class="iconify text-celadon" data-icon="mdi:home-city-outline" data-width="20"></span>
                </div>
                <div>
                  <h4 class="font-semibold text-lightNeutral">Home Baazar</h4>
                  <span class="text-[10px] uppercase tracking-wider text-celadon">Brand Identity & Social Media</span>
                </div>
              </div>
              <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
                Designed complete brand identity and managed social media marketing, driving a 55% increase in organic traffic and consistent lead generation.
              </p>
            </div>
          </div>

          <!-- Company 3 -->
          <div class="relative pl-16">
            <div class="absolute left-3.5 top-1 w-5 h-5 bg-celadon rounded-full border-4 border-bgBlack"></div>
            <div class="card-hover bg-darkSurface/50 border border-white/5 rounded-2xl p-6">
              <div class="flex items-center gap-3 mb-3">
                <div class="w-10 h-10 bg-celadon/10 rounded-lg flex items-center justify-center">
                  <span class="iconify text-celadon" data-icon="mdi:web" data-width="20"></span>
                </div>
                <div>
                  <h4 class="font-semibold text-lightNeutral">Basa-Vara.com</h4>
                  <span class="text-[10px] uppercase tracking-wider text-celadon">Digital Campaigns & Creative Design</span>
                </div>
              </div>
              <p class="text-sm font-light text-lightNeutral/50 leading-relaxed">
                Executed targeted ad campaigns and created high-converting visual content, contributing to a 60% boost in user acquisition and brand recall.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== ACHIEVEMENTS ========== -->
  <section class="relative py-20 px-6 lg:px-12 border-y border-white/5">
    <div class="max-w-[80rem] mx-auto">
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
        <div class="scroll-reveal">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-celadon mb-2">100+</div>
          <div class="text-xs uppercase tracking-[0.2em] text-lightNeutral/50">Projects Completed</div>
        </div>
        <div class="scroll-reveal">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-celadon mb-2">5+</div>
          <div class="text-xs uppercase tracking-[0.2em] text-lightNeutral/50">Countries Served</div>
        </div>
        <div class="scroll-reveal">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-celadon mb-2">98%</div>
          <div class="text-xs uppercase tracking-[0.2em] text-lightNeutral/50">Client Satisfaction</div>
        </div>
        <div class="scroll-reveal">
          <div class="text-4xl lg:text-5xl font-light tracking-tighter text-celadon mb-2">24h</div>
          <div class="text-xs uppercase tracking-[0.2em] text-lightNeutral/50">Avg. Response Time</div>
        </div>
      </div>
      <!-- Client countries -->
      <div class="mt-12 flex flex-wrap justify-center gap-3 scroll-reveal">
        <span class="text-xs font-light text-lightNeutral/40 border border-white/10 rounded-full px-4 py-1.5">🇬🇧 United Kingdom</span>
        <span class="text-xs font-light text-lightNeutral/40 border border-white/10 rounded-full px-4 py-1.5">🇺🇸 United States</span>
        <span class="text-xs font-light text-lightNeutral/40 border border-white/10 rounded-full px-4 py-1.5">🇨🇦 Canada</span>
        <span class="text-xs font-light text-lightNeutral/40 border border-white/10 rounded-full px-4 py-1.5">🇧🇩 Bangladesh</span>
        <span class="text-xs font-light text-lightNeutral/40 border border-white/10 rounded-full px-4 py-1.5">🇮🇳 India</span>
      </div>
    </div>
  </section>

  <!-- ========== PORTFOLIO ========== -->
  <section id="portfolio" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="max-w-[80rem] mx-auto">
      <div class="text-center mb-16 scroll-reveal">
        <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">Portfolio</span>
        <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight">
          Selected <span class="text-celadon">Works</span>
        </h2>
        <p class="text-base font-light text-lightNeutral/50 mt-4 max-w-xl mx-auto">
          A curated collection of projects showcasing the intersection of design and marketing strategy.
        </p>
      </div>

      <!-- Filter Buttons -->
      <div class="flex flex-wrap justify-center gap-3 mb-12 scroll-reveal">
        <button onclick="filterPortfolio('all')" class="portfolio-filter active text-xs uppercase tracking-wider font-semibold px-5 py-2.5 rounded-full border border-celadon/30 text-celadon bg-celadon/10 transition-all duration-300" data-filter="all">All</button>
        <button onclick="filterPortfolio('design')" class="portfolio-filter text-xs uppercase tracking-wider font-semibold px-5 py-2.5 rounded-full border border-white/10 text-lightNeutral/50 hover:border-celadon/30 hover:text-celadon transition-all duration-300" data-filter="design">Design</button>
        <button onclick="filterPortfolio('marketing')" class="portfolio-filter text-xs uppercase tracking-wider font-semibold px-5 py-2.5 rounded-full border border-white/10 text-lightNeutral/50 hover:border-celadon/30 hover:text-celadon transition-all duration-300" data-filter="marketing">Marketing</button>
        <button onclick="filterPortfolio('branding')" class="portfolio-filter text-xs uppercase tracking-wider font-semibold px-5 py-2.5 rounded-full border border-white/10 text-lightNeutral/50 hover:border-celadon/30 hover:text-celadon transition-all duration-300" data-filter="branding">Branding</button>
      </div>

      <!-- Portfolio Grid -->
      <div id="portfolioGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Project 1 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="design">
          <img src="https://picsum.photos/seed/youtube-thumb-design/600/450.jpg" alt="YouTube Thumbnail Series" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Graphic Design</span>
            <h3 class="text-lg font-semibold mb-2">YouTube Thumbnail Series</h3>
            <p class="text-sm font-light text-lightNeutral/60">Designed 50+ high-CTR thumbnails for content creators, averaging 12% click-through rate improvement.</p>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="branding">
          <img src="https://picsum.photos/seed/homebaazar-brand/600/450.jpg" alt="Home Baazar Rebrand" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Brand Identity</span>
            <h3 class="text-lg font-semibold mb-2">Home Baazar — Full Rebrand</h3>
            <p class="text-sm font-light text-lightNeutral/60">Complete visual identity overhaul including logo, color system, typography, and brand guidelines.</p>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="marketing">
          <img src="https://picsum.photos/seed/social-campaign-results/600/450.jpg" alt="Social Media Campaign" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Digital Marketing</span>
            <h3 class="text-lg font-semibold mb-2">Basavara.com Growth Campaign</h3>
            <p class="text-sm font-light text-lightNeutral/60">End-to-end social media campaign that drove 60% increase in user acquisition within 3 months.</p>
          </div>
        </div>

        <!-- Project 4 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="design">
          <img src="https://picsum.photos/seed/tshirt-merch-collection/600/450.jpg" alt="T-shirt Merch Line" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Merchandise Design</span>
            <h3 class="text-lg font-semibold mb-2">Streetwear T-shirt Collection</h3>
            <p class="text-sm font-light text-lightNeutral/60">Designed a 15-piece apparel collection blending typography and illustration for a D2C fashion brand.</p>
          </div>
        </div>

        <!-- Project 5 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="marketing">
          <img src="https://picsum.photos/seed/arifin-digital-marketing/600/450.jpg" alt="Arifin Tech Campaign" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Digital Marketing</span>
            <h3 class="text-lg font-semibold mb-2">Arifin Tech — Lead Generation</h3>
            <p class="text-sm font-light text-lightNeutral/60">Multi-channel marketing strategy combining Google Ads & social media for B2B lead generation.</p>
          </div>
        </div>

        <!-- Project 6 -->
        <div class="scroll-reveal portfolio-item group rounded-2xl overflow-hidden border border-white/5 relative cursor-pointer" data-category="branding design">
          <img src="https://picsum.photos/seed/social-media-visual-pack/600/450.jpg" alt="Social Media Design System" class="portfolio-img w-full h-72 object-cover">
          <div class="overlay absolute inset-0 bg-bgBlack/80 backdrop-blur-sm flex flex-col justify-end p-6">
            <span class="text-[10px] uppercase tracking-[0.2em] text-celadon mb-2">Design + Branding</span>
            <h3 class="text-lg font-semibold mb-2">Social Media Design System</h3>
            <p class="text-sm font-light text-lightNeutral/60">Created a scalable visual design system for consistent brand presence across 4 social platforms.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== TESTIMONIALS / QUOTE ========== -->
  <section class="relative py-20 px-6 lg:px-12 border-y border-white/5 overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-r from-celadon/5 via-transparent to-purple-500/5"></div>
    <div class="max-w-4xl mx-auto text-center relative scroll-reveal">
      <span class="iconify text-celadon/30 mb-6 inline-block" data-icon="mdi:format-quote-open" data-width="48"></span>
      <blockquote class="text-xl lg:text-2xl font-light text-lightNeutral/80 leading-relaxed italic mb-6">
        Great design doesn't just look good — it solves problems, tells stories, and drives action. That's the philosophy I bring to every project.
      </blockquote>
      <div class="flex items-center justify-center gap-3">
        <div class="w-10 h-10 bg-celadon/20 rounded-full flex items-center justify-center">
          <span class="text-celadon text-sm font-bold">S</span>
        </div>
        <div class="text-left">
          <div class="text-sm font-medium text-lightNeutral">Srabon Chandra Das</div>
          <div class="text-xs text-lightNeutral/40">Digital Marketer & Graphic Designer</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== CTA / CONTACT ========== -->
  <section id="contact" class="relative py-24 lg:py-32 px-6 lg:px-12">
    <div class="absolute top-0 left-1/4 w-80 h-80 bg-celadon/10 rounded-full blob blob-1" style="filter:blur(100px)"></div>
    <div class="absolute bottom-0 right-1/4 w-72 h-72 bg-purple-500/10 rounded-full blob blob-3" style="filter:blur(100px)"></div>

    <div class="max-w-[80rem] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
        <!-- Left CTA -->
        <div class="scroll-reveal">
          <span class="text-[10px] uppercase tracking-[0.25em] text-celadon font-medium mb-4 block">Get In Touch</span>
          <h2 class="text-3xl lg:text-5xl font-bold leading-tight tracking-tight mb-6">
            Let's Create<br>Something <span class="text-celadon">Amazing</span>
          </h2>
          <p class="text-base font-light text-lightNeutral/50 leading-relaxed mb-8">
            Whether you need a stunning brand identity, scroll-stopping social media content, or a data-driven marketing strategy — I'm ready to bring your vision to life. Let's talk about your next project.
          </p>
          <div class="flex flex-col gap-4 mb-8">
            <a href="mailto:srabon@example.com" class="flex items-center gap-4 group">
              <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center group-hover:bg-celadon/20 transition-colors duration-300">
                <span class="iconify text-celadon" data-icon="mdi:email-outline" data-width="22"></span>
              </div>
              <div>
                <div class="text-xs text-lightNeutral/40 uppercase tracking-wider">Email</div>
                <div class="text-sm text-lightNeutral group-hover:text-celadon transition-colors">srabon@example.com</div>
              </div>
            </a>
            <a href="#" class="flex items-center gap-4 group">
              <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center group-hover:bg-celadon/20 transition-colors duration-300">
                <span class="iconify text-celadon" data-icon="mdi:whatsapp" data-width="22"></span>
              </div>
              <div>
                <div class="text-xs text-lightNeutral/40 uppercase tracking-wider">WhatsApp</div>
                <div class="text-sm text-lightNeutral group-hover:text-celadon transition-colors">Available for quick chats</div>
              </div>
            </a>
            <a href="#" class="flex items-center gap-4 group">
              <div class="w-12 h-12 bg-celadon/10 rounded-xl flex items-center justify-center group-hover:bg-celadon/20 transition-colors duration-300">
                <span class="iconify text-celadon" data-icon="mdi:linkedin" data-width="22"></span>
              </div>
              <div>
                <div class="text-xs text-lightNeutral/40 uppercase tracking-wider">LinkedIn</div>
                <div class="text-sm text-lightNeutral group-hover:text-celadon transition-colors">Let's connect professionally</div>
              </div>
            </a>
          </div>
        </div>

        <!-- Right Contact Form -->
        <div class="scroll-reveal">
          <form id="contactForm" class="bg-darkSurface/50 border border-white/5 rounded-2xl p-8 space-y-5">
            <div>
              <label class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/40 mb-2 block">Your Name</label>
              <input type="text" id="formName" placeholder="John Doe" class="w-full bg-bgBlack/60 border border-white/10 rounded-xl px-5 py-3.5 text-sm text-lightNeutral placeholder-lightNeutral/20 focus:outline-none focus:border-celadon/50 transition-colors duration-300">
            </div>
            <div>
              <label class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/40 mb-2 block">Email Address</label>
              <input type="email" id="formEmail" placeholder="john@company.com" class="w-full bg-bgBlack/60 border border-white/10 rounded-xl px-5 py-3.5 text-sm text-lightNeutral placeholder-lightNeutral/20 focus:outline-none focus:border-celadon/50 transition-colors duration-300">
            </div>
            <div>
              <label class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/40 mb-2 block">Project Type</label>
              <select id="formType" class="w-full bg-bgBlack/60 border border-white/10 rounded-xl px-5 py-3.5 text-sm text-lightNeutral/60 focus:outline-none focus:border-celadon/50 transition-colors duration-300 appearance-none cursor-pointer">
                <option value="">Select a service</option>
                <option value="thumbnail">YouTube Thumbnail Design</option>
                <option value="branding">Logo & Brand Identity</option>
                <option value="social">Social Media Design</option>
                <option value="merch">T-shirt & Merch Design</option>
                <option value="marketing">Digital Marketing</option>
                <option value="launch">Complete Brand Launch</option>
              </select>
            </div>
            <div>
              <label class="text-[10px] uppercase tracking-[0.2em] text-lightNeutral/40 mb-2 block">Your Message</label>
              <textarea id="formMessage" rows="4" placeholder="Tell me about your project..." class="w-full bg-bgBlack/60 border border-white/10 rounded-xl px-5 py-3.5 text-sm text-lightNeutral placeholder-lightNeutral/20 focus:outline-none focus:border-celadon/50 transition-colors duration-300 resize-none"></textarea>
            </div>
            <button type="submit" class="magnetic-btn w-full text-sm font-semibold uppercase tracking-wider border border-celadon text-celadon px-8 py-4 rounded-full flex items-center justify-center gap-2">
              Send Message
              <span class="iconify" data-icon="mdi:send" data-width="18"></span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- ========== FOOTER ========== -->
  <footer class="border-t border-white/5 py-12 px-6 lg:px-12">
    <div class="max-w-[80rem] mx-auto">
      <div class="flex flex-col md:flex-row items-center justify-between gap-6">
        <div>
          <a href="#hero" class="text-xl font-bold tracking-tight text-lightNeutral">
            <span class="text-celadon">S</span>rabon<span class="text-celadon">.</span>
          </a>
          <p class="text-xs text-lightNeutral/30 mt-1">Digital Marketer & Graphic Designer</p>
        </div>
        <div class="flex items-center gap-6">
          <a href="#" class="text-lightNeutral/30 hover:text-celadon transition-colors duration-300">
            <span class="iconify" data-icon="mdi:linkedin" data-width="20"></span>
          </a>
          <a href="#" class="text-lightNeutral/30 hover:text-celadon transition-colors duration-300">
            <span class="iconify" data-icon="mdi:instagram" data-width="20"></span>
          </a>
          <a href="#" class="text-lightNeutral/30 hover:text-celadon transition-colors duration-300">
            <span class="iconify" data-icon="mdi:twitter" data-width="20"></span>
          </a>
          <a href="#" class="text-lightNeutral/30 hover:text-celadon transition-colors duration-300">
            <span class="iconify" data-icon="mdi:facebook" data-width="20"></span>
          </a>
        </div>
        <p class="text-xs text-lightNeutral/20">© 2025 Srabon Chandra Das. All rights reserved.</p>
      </div>
    </div>
  </footer>

  <!-- Toast Notification -->
  <div id="toast" class="toast">
    <div class="flex items-center gap-3">
      <span class="iconify text-celadon" data-icon="mdi:check-circle" data-width="20"></span>
      <span id="toastMsg" class="text-sm">Message sent successfully!</span>
    </div>
  </div>

  <script>
    // ===== NAVBAR SCROLL =====
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 80) {
        navbar.classList.add('py-3', 'bg-bgBlack/80', 'backdrop-blur-xl', 'border-b', 'border-white/5');
        navbar.classList.remove('py-6', 'lg:py-8');
      } else {
        navbar.classList.remove('py-3', 'bg-bgBlack/80', 'backdrop-blur-xl', 'border-b', 'border-white/5');
        navbar.classList.add('py-6', 'lg:py-8');
      }
    });

    // ===== MOBILE MENU =====
    function toggleMenu() {
      document.getElementById('mobileMenu').classList.toggle('open');
    }

    // ===== SCROLL REVEAL =====
    const revealElements = document.querySelectorAll('.scroll-reveal');
    const revealObserver = new IntersectionObserver((entries) => {
      entries.forEach((entry, index) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            entry.target.classList.add('revealed');
          }, index * 80);
          revealObserver.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });

    revealElements.forEach(el => revealObserver.observe(el));

    // ===== COUNTER ANIMATION =====
    const counterElements = document.querySelectorAll('.counter-num');
    const counterObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const target = parseInt(entry.target.dataset.target);
          let current = 0;
          const increment = target / 60;
          const timer = setInterval(() => {
            current += increment;
            if (current >= target) {
              entry.target.textContent = target + '+';
              clearInterval(timer);
            } else {
              entry.target.textContent = Math.floor(current) + '+';
            }
          }, 25);
          counterObserver.unobserve(entry.target);
        }
      });
    }, { threshold: 0.5 });

    counterElements.forEach(el => counterObserver.observe(el));

    // ===== PORTFOLIO FILTER =====
    function filterPortfolio(category) {
      const items = document.querySelectorAll('.portfolio-item');
      const buttons = document.querySelectorAll('.portfolio-filter');

      buttons.forEach(btn => {
        btn.classList.remove('bg-celadon/10', 'border-celadon/30', 'text-celadon');
        btn.classList.add('border-white/10', 'text-lightNeutral/50');
      });
      const activeBtn = document.querySelector(`[data-filter="${category}"]`);
      activeBtn.classList.add('bg-celadon/10', 'border-celadon/30', 'text-celadon');
      activeBtn.classList.remove('border-white/10', 'text-lightNeutral/50');

      items.forEach(item => {
        const cats = item.dataset.category;
        if (category === 'all' || cats.includes(category)) {
          item.style.display = 'block';
          item.style.opacity = '0';
          item.style.transform = 'translateY(20px)';
          setTimeout(() => {
            item.style.transition = 'all 0.5s ease';
            item.style.opacity = '1';
            item.style.transform = 'translateY(0)';
          }, 50);
        } else {
          item.style.transition = 'all 0.3s ease';
          item.style.opacity = '0';
          item.style.transform = 'translateY(20px)';
          setTimeout(() => {
            item.style.display = 'none';
          }, 300);
        }
      });
    }

    // ===== CONTACT FORM =====
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('formName').value.trim();
      const email = document.getElementById('formEmail').value.trim();
      const message = document.getElementById('formMessage').value.trim();

      if (!name || !email || !message) {
        showToast('Please fill in all required fields.', 'error');
        return;
      }

      // Simulate sending
      const btn = this.querySelector('button[type="submit"]');
      const originalText = btn.innerHTML;
      btn.innerHTML = '<span class="iconify animate-spin" data-icon="mdi:loading" data-width="18"></span> Sending...';
      btn.disabled = true;

      setTimeout(() => {
        btn.innerHTML = originalText;
        btn.disabled = false;
        this.reset();
        showToast('Message sent successfully! I\'ll get back to you soon.', 'success');
      }, 1500);
    });

    // ===== TOAST =====
    function showToast(msg, type) {
      const toast = document.getElementById('toast');
      const toastMsg = document.getElementById('toastMsg');
      toastMsg.textContent = msg;

      if (type === 'error') {
        toast.style.borderColor = 'rgba(239,68,68,0.3)';
      } else {
        toast.style.borderColor = 'rgba(156,220,170,0.3)';
      }

      toast.classList.add('show');
      setTimeout(() => {
        toast.classList.remove('show');
      }, 3500);
    }

    // ===== SMOOTH SCROLL =====
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });

    // ===== SPIN KEYFRAME (for decorative ring) =====
    // Already handled by CSS, but let's add the keyframe dynamically
    const style = document.createElement('style');
    style.textContent = `@keyframes spin { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }`;
    document.head.appendChild(style);
  </script>

</body>
</html>
