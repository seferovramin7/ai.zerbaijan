<script setup>
import { ref } from 'vue'

const registerUrl = 'https://docs.google.com/forms/d/e/1FAIpQLSd-register-example'

const faqs = [
  {
    q: 'ai.zerbaijan nədir?',
    a: 'Azərbaycan dilində süni intellekt öyrənmək üçün yaradılmış açıq icmadır. Tədbirlər, vebinarlar və layihələrlə birlikdə öyrənirik.'
  },
  {
    q: 'İcmaya necə qoşula bilərəm?',
    a: '“Qeydiyyatdan keç” düyməsinə klikləyin və formu doldurun. Komandamız sizi növbəti tədbirlər üçün dəvət edəcək.'
  },
  {
    q: 'Tədbirlər ödənişlidir?',
    a: 'İlk vebinar və icma görüşləri pulsuzdur. Kurslar və uzunmüddətli proqramlar haqqında məlumat ayrıca paylaşılacaq.'
  },
  {
    q: 'Dil dəstəyi necədir?',
    a: 'Bütün kontent Azərbaycan dilindədir. Terminlər beynəlxalq standartlara uyğun təqdim olunur.'
  }
]

const openFaqIdx = ref(-1)
const toggleFaq = (idx) => {
  openFaqIdx.value = openFaqIdx.value === idx ? -1 : idx
}
</script>

<template>
  <header class="topbar">
    <div class="topbar-inner container">
      <a href="#" class="brand" aria-label="ai.zerbaijan — ana səhifə">
        <img src="/aizerbaijan.jpg" alt="ai.zerbaijan loqo" class="brand-logo" />
      </a>
      <nav class="nav">
        <a href="#about">Haqqımızda</a>
        <a href="#programs">Proqramlar</a>
        <a href="#webinars">Vebinar</a>
        <a href="articles/">Məqalələr</a>
        <a href="#resources">Resurslar</a>
        <a href="#faq">Suallar</a>
        <a :href="registerUrl" target="_blank" rel="noopener" class="btn primary" style="padding:.55rem .9rem">Qoşul</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section class="section">
      <div class="container hero-surface">
      <div class="hero">
        <p></p>
        <div>
          <div class="pill" style="margin-bottom:.6rem">
            <span class="icon-circle">✨</span>
            <span>Azərbaycan dilində AI icması</span>
          </div>
          <h1 class="hero-title">Öyrən, paylaş, qur</h1>
          <p class="hero-sub">Vebinarlar, görüşlər, kurslar və real layihələrlə süni intellekti birlikdə öyrənirik. Hamı üçün açıq və dəstəkləyici mühit.</p>
          <div style="margin-top:1rem; display:flex; gap:.6rem; flex-wrap:wrap;">
            <a class="btn primary" :href="registerUrl" target="_blank" rel="noopener">İcmaya qoşul</a>
            <a class="btn ghost" href="#webinars">Yaxın vebinar</a>
            <a class="btn ghost" href="articles/">Məqalələr</a>
          </div>
        </div>
      </div>
      </div>
    </section>

    <!-- Benefits -->
    <section id="benefits" class="section container">
      <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:1rem">Niyə qoşulmağa dəyər?</h2>
      <div class="grid-3">
        <div class="card feature">
          <div class="icon-circle">🎥</div>
          <div>
            <h3 style="font-weight:700; margin-bottom:.4rem">Canlı vebinarlar</h3>
            <p class="muted">Mütəxəssislərlə LLM-lər, kompüter görməsi, MLOps və s. mövzularda praktiki sessiyalar.</p>
            <div class="divider"></div>
            <a class="btn ghost" href="articles/generativ-ai-prompt.html">Daha çox oxu</a>
          </div>
        </div>
        <div class="card feature">
          <div class="icon-circle">🧪</div>
          <div>
            <h3 style="font-weight:700; margin-bottom:.4rem">Praktiki kurslar</h3>
            <p class="muted">Layihəyönümlü dərslər və kod laboratoriyaları ilə sıfırdan tətbiqlər qur.</p>
            <div class="divider"></div>
            <a class="btn ghost" href="articles/mashin-oyrenmesi-baslanqic.html">Başlama bələdçisi</a>
          </div>
        </div>
        <div class="card feature">
          <div class="icon-circle">🤝</div>
          <div>
            <h3 style="font-weight:700; margin-bottom:.4rem">İcma və karyera</h3>
            <p class="muted">Networking, mentorluq, açıq mənbə layihələri və karyera dəstəyi.</p>
            <div class="divider"></div>
            <a class="btn ghost" href="articles/mlops-nedir.html">MLOps nədir?</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats -->
    <section class="section container">
      <div class="grid-3">
        <div class="card stat"><div class="stat-num">21</div><div class="muted">avqust — ilk vebinar</div></div>
        <div class="card stat"><div class="stat-num">100%</div><div class="muted">Azərbaycan dilində məzmun</div></div>
        <div class="card stat"><div class="stat-num">Açıq</div><div class="muted">hamı üçün əlçatan icma</div></div>
      </div>
    </section>

    <!-- About -->
    <section id="about" class="section container">
      <div class="card">
        <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:.6rem">Haqqımızda</h2>
        <p class="muted">ai.zerbaijan könüllülərin yaratdığı bilik mərkəzidir. Məqsədimiz Azərbaycan dilində keyfiyyətli resurslar toplamaq, yerli mütəxəssisləri bir araya gətirmək və hamı üçün əlçatan öyrənmə mühiti yaratmaqdır.</p>
      </div>
    </section>

    <!-- Programs -->
    <section id="programs" class="section container">
      <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:1rem">Proqramlarımız</h2>
      <div class="grid-3">
        <div class="card">
          <span class="kicker">Format</span>
          <h3 style="font-weight:700; margin:.3rem 0 .5rem">Vebinarlar</h3>
          <p class="muted">İnteraktiv sessiyalar, canlı demo və Q&A.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="#webinars">Yaxın vebinar</a>
          <a class="btn ghost" href="articles/generativ-ai-prompt.html" style="margin-left:.5rem">Prompt təlimi</a>
        </div>
        <div class="card">
          <span class="kicker">Öyrənmə</span>
          <h3 style="font-weight:700; margin:.3rem 0 .5rem">Kurslar</h3>
          <p class="muted">Mentorluqla layihə əsaslı tədris, portfolio üçün tapşırıqlar.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="articles/mashin-oyrenmesi-baslanqic.html">Başlamaq üçün plan</a>
        </div>
        <div class="card">
          <span class="kicker">İcma</span>
          <h3 style="font-weight:700; margin:.3rem 0 .5rem">Görüşlər və layihələr</h3>
          <p class="muted">Onlayn görüşlər, açıq mənbə töhfələri, hackday-lər.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="articles/mlops-nedir.html">İstehsalda ML</a>
        </div>
      </div>
    </section>

    <!-- Webinars -->
    <section id="webinars" class="section container">
      <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:1rem">Yaxın vebinar</h2>
      <div class="card" style="display:grid; gap:.6rem">
        <div style="display:flex; justify-content:space-between; gap:.75rem; flex-wrap:wrap; align-items:center;">
          <div>
            <div class="badge" style="margin-bottom:.4rem">21 avqust</div>
            <div style="font-weight:700">Generativ AI ilə Sürətli Prototipləmə</div>
            <div class="muted">Başlanğıc səviyyədən mütəxəssisə qədər praktik yanaşma. Q&A sessiyası daxil.</div>
          </div>
          <a class="btn primary" :href="registerUrl" target="_blank" rel="noopener">Qeydiyyatdan keç</a>
        </div>
      </div>
      <p class="center muted" style="margin-top:1rem">Yeni tədbirlər üçün bizi izləyin.</p>
    </section>

    <!-- Resources -->
    <section id="resources" class="section container">
      <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:1rem">Resurslar</h2>
      <div class="grid-3">
        <div class="card">
          <h3 style="font-weight:700; margin-bottom:.4rem">Başlanğıc bələdçisi</h3>
          <p class="muted">Python, Jupyter, əsas ML anlayışları və generativ AI ilə sürətli başlanğıc.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="articles/mashin-oyrenmesi-baslanqic.html">Oxu</a>
        </div>
        <div class="card">
          <h3 style="font-weight:700; margin-bottom:.4rem">Tədris planı</h3>
          <p class="muted">LLM-lər, incə tənzimləmə, məlumatların hazırlanması, qiymətləndirmə və yerləşdirmə.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="articles/llm-nedir.html">LLM nədir?</a>
        </div>
        <div class="card">
          <h3 style="font-weight:700; margin-bottom:.4rem">İcma qaydaları</h3>
          <p class="muted">Hörmət, inklüzivlik və paylaşım mədəniyyəti. Hər kəs üçün təhlükəsiz məkan.</p>
          <div class="divider"></div>
          <a class="btn ghost" href="articles/ai-nedir.html">AI nədir?</a>
        </div>
      </div>
    </section>

    <!-- FAQ -->
    <section id="faq" class="section container">
      <h2 style="font-size:1.6rem; font-weight:800; margin-bottom:1rem">Tez-tez verilən suallar</h2>
      <div class="faq-list">
        <div v-for="(item, idx) in faqs" :key="idx" class="faq-item card" @click="toggleFaq(idx)">
          <div style="display:flex; justify-content:space-between; align-items:center; gap:1rem;">
            <div style="font-weight:600">{{ item.q }}</div>
            <div class="muted">{{ openFaqIdx === idx ? '−' : '+' }}</div>
          </div>
          <div v-if="openFaqIdx === idx" class="muted" style="margin-top:.5rem;">{{ item.a }}</div>
        </div>
      </div>
    </section>

    <!-- Newsletter / CTA -->
    <section id="contact" class="section container">
      <div class="card" style="display:grid; gap:.8rem;">
        <h2 style="font-size:1.4rem; font-weight:800">Gözləmə siyahısına yazıl</h2>
        <p class="muted">Yeni vebinar və kurslardan ilk xəbərdar olmaq üçün qeydiyyatdan keç.</p>
        <div class="input-group">
          <input type="email" placeholder="E-poçt ünvanınız" class="input" aria-label="E-poçt" />
          <a class="btn primary" :href="registerUrl" target="_blank" rel="noopener">Abunə ol</a>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <section class="section container center">
      <p class="muted">© {{ new Date().getFullYear() }} ai.zerbaijan — açıq icma. · <a href="articles/">Məqalələr</a></p>
    </section>
  </main>
</template>

<style scoped>
</style>
