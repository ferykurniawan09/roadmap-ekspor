[roadmap-ekspor-saudi.docx](https://github.com/user-attachments/files/27228775/roadmap-ekspor-saudi.docx)
[timeline-ekspor-saudi.html](https://github.com/user-attachments/files/27228777/timeline-ekspor-saudi.html)
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Roadmap Ekspor 6 Bulan — Indonesia ke Arab Saudi</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=IBM+Plex+Mono:wght@300;400;500&family=Tajawal:wght@300;400;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }

:root {
  --bg: #0a0f0d;
  --surface: #111812;
  --border: #1e2e22;
  --gold: #c8a45a;
  --gold-light: #e8c87a;
  --gold-dim: rgba(200,164,90,0.12);
  --green: #2d6a4f;
  --green-bright: #52b788;
  --text: #e8e0d0;
  --muted: #7a8a7e;
  --white: #f5f0e8;
  --red: #c0392b;
  --m1: #c8a45a;
  --m2: #52b788;
  --m3: #4a90d9;
  --m4: #9b59b6;
  --m5: #e67e22;
  --m6: #e74c3c;
}

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'IBM Plex Mono', monospace;
  min-height: 100vh;
  overflow-x: hidden;
}

/* ─── HEADER ─── */
header {
  background: linear-gradient(180deg, #050a07 0%, var(--bg) 100%);
  padding: 40px 20px 30px;
  text-align: center;
  position: relative;
  border-bottom: 1px solid var(--border);
}

.ornament {
  font-size: 11px;
  letter-spacing: 6px;
  color: var(--gold);
  text-transform: uppercase;
  opacity: 0.8;
  margin-bottom: 12px;
  font-family: 'Tajawal', sans-serif;
}

header h1 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(26px, 6vw, 44px);
  font-weight: 700;
  color: var(--white);
  line-height: 1.1;
  margin-bottom: 8px;
}

header h1 em {
  font-style: italic;
  color: var(--gold);
}

header p {
  font-size: 11px;
  color: var(--muted);
  letter-spacing: 2px;
  text-transform: uppercase;
}

.flags { font-size: 22px; letter-spacing: 8px; margin: 10px 0 4px; }

/* ─── PROGRESS GLOBAL ─── */
.global-progress {
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  padding: 14px 20px;
  position: sticky;
  top: 0;
  z-index: 200;
  display: flex;
  align-items: center;
  gap: 14px;
}

.gp-label {
  font-size: 10px;
  color: var(--gold);
  letter-spacing: 2px;
  text-transform: uppercase;
  white-space: nowrap;
  flex-shrink: 0;
}

.gp-bar {
  flex: 1;
  height: 4px;
  background: var(--border);
  border-radius: 2px;
  overflow: hidden;
}

.gp-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--gold), var(--green-bright));
  border-radius: 2px;
  width: 0%;
  transition: width 0.6s cubic-bezier(0.4,0,0.2,1);
}

.gp-pct {
  font-size: 11px;
  color: var(--gold);
  font-weight: 500;
  white-space: nowrap;
  flex-shrink: 0;
  min-width: 36px;
  text-align: right;
}

/* ─── PHASE TABS ─── */
.phase-nav {
  display: flex;
  overflow-x: auto;
  gap: 0;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  padding: 0 12px;
  scrollbar-width: none;
}
.phase-nav::-webkit-scrollbar { display: none; }

.phase-tab {
  flex-shrink: 0;
  padding: 10px 14px;
  font-size: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: var(--muted);
  cursor: pointer;
  border-bottom: 2px solid transparent;
  transition: all 0.2s;
  white-space: nowrap;
  font-family: 'IBM Plex Mono', monospace;
}

.phase-tab:hover { color: var(--text); }
.phase-tab.active { color: var(--gold); border-bottom-color: var(--gold); }

/* ─── MAIN ─── */
main { max-width: 720px; margin: 0 auto; padding: 24px 16px 60px; }

/* ─── MONTH BLOCK ─── */
.month-block {
  margin-bottom: 28px;
  display: none;
  animation: fadeUp 0.4s ease both;
}

.month-block.visible { display: block; }

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}

.month-header {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 14px;
}

.month-number {
  font-family: 'Cormorant Garamond', serif;
  font-size: 52px;
  font-weight: 700;
  line-height: 1;
  color: var(--month-color);
  opacity: 0.18;
  flex-shrink: 0;
  width: 52px;
  text-align: center;
}

.month-info { flex: 1; }

.month-label {
  font-size: 10px;
  color: var(--month-color);
  letter-spacing: 3px;
  text-transform: uppercase;
  margin-bottom: 3px;
}

.month-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 20px;
  font-weight: 600;
  color: var(--white);
  line-height: 1.2;
}

.month-sub {
  font-size: 10px;
  color: var(--muted);
  margin-top: 2px;
}

.month-progress {
  text-align: right;
  flex-shrink: 0;
}

.mp-ring {
  width: 40px;
  height: 40px;
  position: relative;
}

.mp-ring svg {
  width: 40px;
  height: 40px;
  transform: rotate(-90deg);
}

.mp-ring circle.bg {
  fill: none;
  stroke: var(--border);
  stroke-width: 3;
}

.mp-ring circle.fill {
  fill: none;
  stroke: var(--month-color);
  stroke-width: 3;
  stroke-linecap: round;
  stroke-dasharray: 100.5;
  stroke-dashoffset: 100.5;
  transition: stroke-dashoffset 0.6s ease;
}

.mp-ring .pct-label {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%,-50%);
  font-size: 9px;
  color: var(--month-color);
  font-weight: 500;
}

/* ─── WEEK SECTION ─── */
.week-section {
  margin-bottom: 10px;
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
  background: var(--surface);
}

.week-header {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px 14px;
  cursor: pointer;
  transition: background 0.15s;
  background: rgba(255,255,255,0.02);
}

.week-header:hover { background: rgba(255,255,255,0.04); }

.week-dot {
  width: 8px; height: 8px;
  border-radius: 50%;
  background: var(--month-color);
  flex-shrink: 0;
  opacity: 0.6;
}

.week-label {
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 2px;
  text-transform: uppercase;
}

.week-title {
  font-size: 12px;
  color: var(--text);
  flex: 1;
  font-weight: 500;
}

.week-count {
  font-size: 10px;
  color: var(--muted);
  flex-shrink: 0;
}

.week-chevron {
  font-size: 10px;
  color: var(--muted);
  transition: transform 0.3s;
  flex-shrink: 0;
}

.week-section.open .week-chevron { transform: rotate(180deg); }

.week-body { display: none; }
.week-section.open .week-body { display: block; }

/* ─── TASK ITEM ─── */
.task-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 11px 14px;
  border-top: 1px solid var(--border);
  cursor: pointer;
  transition: background 0.15s;
}

.task-item:hover { background: rgba(255,255,255,0.03); }
.task-item.done { background: rgba(82,183,136,0.04); }

.task-check {
  width: 18px; height: 18px;
  border: 1.5px solid var(--border);
  border-radius: 4px;
  flex-shrink: 0;
  margin-top: 1px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s;
  background: transparent;
}

.task-item.done .task-check {
  background: var(--green-bright);
  border-color: var(--green-bright);
}

.task-tick { color: #fff; font-size: 10px; display: none; }
.task-item.done .task-tick { display: block; }

.task-content { flex: 1; min-width: 0; }

.task-name {
  font-size: 12px;
  color: var(--text);
  line-height: 1.4;
  font-weight: 400;
}

.task-item.done .task-name {
  color: var(--muted);
  text-decoration: line-through;
}

.task-detail {
  font-size: 10.5px;
  color: var(--muted);
  margin-top: 3px;
  line-height: 1.5;
  font-family: 'IBM Plex Mono', monospace;
}

.task-badge {
  font-size: 9px;
  font-weight: 500;
  padding: 2px 7px;
  border-radius: 10px;
  flex-shrink: 0;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  margin-top: 1px;
}

.badge-wajib { background: rgba(192,57,43,0.15); color: #e74c3c; border: 1px solid rgba(192,57,43,0.3); }
.badge-halal { background: rgba(45,106,79,0.2); color: var(--green-bright); border: 1px solid rgba(45,106,79,0.4); }
.badge-bisnis { background: rgba(200,164,90,0.12); color: var(--gold); border: 1px solid rgba(200,164,90,0.3); }
.badge-logistik { background: rgba(74,144,217,0.12); color: #4a90d9; border: 1px solid rgba(74,144,217,0.3); }

/* ─── MILESTONE CARD ─── */
.milestone {
  background: linear-gradient(135deg, rgba(200,164,90,0.08), rgba(45,106,79,0.08));
  border: 1px solid rgba(200,164,90,0.25);
  border-radius: 8px;
  padding: 14px 16px;
  margin-top: 10px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.ms-icon { font-size: 22px; flex-shrink: 0; }

.ms-content { flex: 1; }

.ms-label {
  font-size: 9px;
  color: var(--gold);
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 3px;
}

.ms-text {
  font-family: 'Cormorant Garamond', serif;
  font-size: 16px;
  color: var(--white);
  font-weight: 600;
}

/* ─── SUMMARY BAR ─── */
.summary {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 16px;
  margin-bottom: 20px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
  text-align: center;
}

.sum-item .val {
  font-family: 'Cormorant Garamond', serif;
  font-size: 28px;
  font-weight: 700;
  color: var(--gold);
  line-height: 1;
}

.sum-item .lbl {
  font-size: 9px;
  color: var(--muted);
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-top: 4px;
}

/* ─── DONE BANNER ─── */
.done-banner {
  display: none;
  background: linear-gradient(135deg, #0f3d22, #1a2e0f);
  border: 1px solid var(--green);
  border-radius: 10px;
  padding: 20px;
  text-align: center;
  margin-top: 20px;
}

.done-banner.show { display: block; }

.done-banner h2 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 24px;
  color: var(--gold-light);
  margin-bottom: 6px;
}

.done-banner p {
  font-size: 11px;
  color: var(--green-bright);
  letter-spacing: 1px;
}

/* ─── RESET BTN ─── */
.reset-btn {
  display: block;
  margin: 24px auto 0;
  background: transparent;
  border: 1px solid var(--border);
  color: var(--muted);
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  padding: 8px 22px;
  border-radius: 20px;
  cursor: pointer;
  letter-spacing: 2px;
  text-transform: uppercase;
  transition: all 0.2s;
}

.reset-btn:hover {
  border-color: var(--gold);
  color: var(--gold);
}

/* divider */
.month-divider {
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--border), transparent);
  margin: 20px 0;
}
</style>
</head>
<body>

<header>
  <div class="ornament">🌙 Roadmap Ekspor Halal · بسم الله</div>
  <h1>6 Bulan Menuju<br><em>First Shipment</em></h1>
  <div class="flags">🇮🇩 ✈️ 🇸🇦</div>
  <p>Step-by-step · Indonesia → Arab Saudi</p>
</header>

<div class="global-progress">
  <span class="gp-label">Total Progress</span>
  <div class="gp-bar"><div class="gp-fill" id="gp-fill"></div></div>
  <span class="gp-pct" id="gp-pct">0%</span>
</div>

<div class="phase-nav" id="phase-nav">
  <div class="phase-tab active" onclick="showPhase('all')">Semua</div>
  <div class="phase-tab" onclick="showPhase('1')" style="--c:var(--m1)">Bln 1</div>
  <div class="phase-tab" onclick="showPhase('2')" style="--c:var(--m2)">Bln 2</div>
  <div class="phase-tab" onclick="showPhase('3')" style="--c:var(--m3)">Bln 3</div>
  <div class="phase-tab" onclick="showPhase('4')" style="--c:var(--m4)">Bln 4</div>
  <div class="phase-tab" onclick="showPhase('5')" style="--c:var(--m5)">Bln 5</div>
  <div class="phase-tab" onclick="showPhase('6')" style="--c:var(--m6)">Bln 6</div>
</div>

<main>

  <div class="summary">
    <div class="sum-item">
      <div class="val" id="sum-done">0</div>
      <div class="lbl">Selesai</div>
    </div>
    <div class="sum-item">
      <div class="val" id="sum-total">0</div>
      <div class="lbl">Total Task</div>
    </div>
    <div class="sum-item">
      <div class="val" id="sum-pct">0%</div>
      <div class="lbl">Progress</div>
    </div>
  </div>

  <!-- ══════════ BULAN 1 ══════════ -->
  <div class="month-block visible" data-month="1" style="--month-color: var(--m1)">
    <div class="month-header">
      <div class="month-number">1</div>
      <div class="month-info">
        <div class="month-label">Bulan Pertama · Pondasi</div>
        <div class="month-title">Legalitas & Riset Produk</div>
        <div class="month-sub">Sebelum jualan, pastikan landasan hukum kuat</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-1">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-1">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section open" id="w1-1">
      <div class="week-header" onclick="toggleWeek('w1-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Riset & Pilih Produk</span>
        <span class="week-count" id="wc-w1-1">0/3</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Tentukan 1 produk fokus ekspor</div>
            <div class="task-detail">Pilih produk yang sudah punya: stok konsisten, bahan halal, bisa diproduksi 100–500kg/bulan minimum.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Riset HS Code produk di bea cukai</div>
            <div class="task-detail">Cek di insw.go.id atau beacukai.go.id. HS Code menentukan tarif bea masuk Saudi & dokumen yang dibutuhkan.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Riset harga pasar Saudi & kompetitor</div>
            <div class="task-detail">Cek di Alibaba, Trademap.org, dan minta info ke ITPC Jeddah. Pastikan harga Anda kompetitif.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w1-2">
      <div class="week-header" onclick="toggleWeek('w1-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Urus Legalitas Dasar</span>
        <span class="week-count" id="wc-w1-2">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Daftar NIB di OSS (oss.go.id)</div>
            <div class="task-detail">Pilih KBLI sesuai produk. Gratis & bisa online. Proses 1–3 hari kerja.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Daftar NPWP & ajukan status PKP</div>
            <div class="task-detail">PKP (Pengusaha Kena Pajak) penting untuk klaim restitusi PPN 0% dari ekspor. Daftar di KPP setempat.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Buka rekening valas (USD/SAR) di bank devisa</div>
            <div class="task-detail">BNI, Mandiri, atau BCA. Bawa NIB, NPWP, dan akta perusahaan. Diperlukan untuk terima pembayaran ekspor.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Aktivasi akun CEISA Bea Cukai (modul ekspor)</div>
            <div class="task-detail">Daftar di portal customer.beacukai.go.id. Wajib untuk pengajuan PEB (dokumen ekspor resmi).</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">🏛️</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 1</div>
        <div class="ms-text">Produk terpilih + semua legalitas dasar selesai</div>
      </div>
    </div>
  </div>

  <div class="month-divider"></div>

  <!-- ══════════ BULAN 2 ══════════ -->
  <div class="month-block visible" data-month="2" style="--month-color: var(--m2)">
    <div class="month-header">
      <div class="month-number">2</div>
      <div class="month-info">
        <div class="month-label">Bulan Kedua · Sertifikasi</div>
        <div class="month-title">Halal & Kesiapan Produk</div>
        <div class="month-sub">Kunci masuk pasar Muslim Saudi — tidak bisa dilewat</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-2">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-2">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w2-1">
      <div class="week-header" onclick="toggleWeek('w2-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Daftar Sertifikasi Halal BPJPH</span>
        <span class="week-count" id="wc-w2-1">0/3</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Daftar di portal halal.go.id (BPJPH/Sihalal)</div>
            <div class="task-detail">Siapkan: NIB, komposisi produk lengkap, daftar bahan baku beserta sertifikat halal supplier-nya.</div>
          </div>
          <span class="task-badge badge-halal">Halal</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Audit internal & dokumentasi SJH (Sistem Jaminan Halal)</div>
            <div class="task-detail">Buat SOP produksi halal: pemisahan bahan, kebersihan alat, daftar supplier halal. Auditor BPJPH akan cek ini.</div>
          </div>
          <span class="task-badge badge-halal">Halal</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Kirim sampel ke lab untuk uji Halal & Sertifikat Analisis (COA)</div>
            <div class="task-detail">Lab terakreditasi: BPOM, LPPOM MUI, atau lab swasta terverifikasi. COA penting untuk buyer Saudi.</div>
          </div>
          <span class="task-badge badge-halal">Halal</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w2-2">
      <div class="week-header" onclick="toggleWeek('w2-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Desain Kemasan Ekspor</span>
        <span class="week-count" id="wc-w2-2">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Desain ulang label dengan teks Arab wajib</div>
            <div class="task-detail">Wajib ada: nama produk, bahan, berat netto, tanggal produksi & kadaluarsa, nama importir Saudi — semua dalam Bahasa Arab.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Cantumkan logo Halal resmi di kemasan</div>
            <div class="task-detail">Logo halal MUI/BPJPH harus cetak offset (bukan stiker). Posisikan di area yang mudah dilihat konsumen.</div>
          </div>
          <span class="task-badge badge-halal">Halal</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Uji kemasan tahan iklim panas (suhu 50°C+)</div>
            <div class="task-detail">Saudi bisa capai 50°C. Test kemasan di suhu tinggi minimal 48 jam. Pertimbangkan foil/laminasi untuk produk pangan.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Buat master karton ekspor (outer carton)</div>
            <div class="task-detail">Label outer carton: HS Code, net/gross weight, dimensi, "Made in Indonesia", tanda fragile jika perlu.</div>
          </div>
          <span class="task-badge badge-logistik">Logistik</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">☪️</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 2</div>
        <div class="ms-text">Pengajuan Halal tersubmit + kemasan siap produksi</div>
      </div>
    </div>
  </div>

  <div class="month-divider"></div>

  <!-- ══════════ BULAN 3 ══════════ -->
  <div class="month-block visible" data-month="3" style="--month-color: var(--m3)">
    <div class="month-header">
      <div class="month-number">3</div>
      <div class="month-info">
        <div class="month-label">Bulan Ketiga · Pemasaran</div>
        <div class="month-title">Cari Buyer & Bangun Profil</div>
        <div class="month-sub">Mulai jangkau pasar Saudi secara aktif</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-3">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-3">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w3-1">
      <div class="week-header" onclick="toggleWeek('w3-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Bangun Profil & Materi Pemasaran</span>
        <span class="week-count" id="wc-w3-1">0/3</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Buat Company Profile & Product Catalogue (Inggris + Arab)</div>
            <div class="task-detail">Sertakan: foto produk profesional, sertifikat halal, kapasitas produksi, MOQ (minimum order quantity), harga FOB.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Daftar & lengkapi profil di Alibaba / Global Sources</div>
            <div class="task-detail">Upload foto HD produk, video pabrik, semua sertifikat. Profil lengkap = 3x lebih banyak inquiry dari buyer.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Buat website/landing page produk (versi Inggris)</div>
            <div class="task-detail">Minimal 1 halaman: produk, sertifikasi, kontak WA/email. Buyer Saudi akan Google nama perusahaan Anda sebelum deal.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w3-2">
      <div class="week-header" onclick="toggleWeek('w3-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Outreach ke Buyer & Lembaga Pemerintah</span>
        <span class="week-count" id="wc-w3-2">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Hubungi ITPC Jeddah & Atase Perdagangan KBRI Riyadh</div>
            <div class="task-detail">Email: itpc.jeddah@kemendag.go.id — Minta database importir Saudi & info pameran dagang. Layanan gratis!</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Kirim email outreach ke min. 20 importir Saudi</div>
            <div class="task-detail">Cari di Kompass Saudi, Yellow Pages Saudi (yellowpages.com.sa), atau database ITPC. Lampirkan catalogue & halal cert.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Daftar program ekspor LPEI / Kemendag</div>
            <div class="task-detail">LPEI punya program pembiayaan & asuransi ekspor untuk UMKM. Kemendag punya program "Matching Buyer" gratis.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Siapkan 10–20 sampel produk siap kirim</div>
            <div class="task-detail">Buyer Saudi SELALU minta sampel. Budget ongkir sampel ke Saudi via DHL: ~Rp500–900rb/kg. Anggap ini investasi.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">🤝</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 3</div>
        <div class="ms-text">Min. 5 leads buyer teridentifikasi + sampel terkirim</div>
      </div>
    </div>
  </div>

  <div class="month-divider"></div>

  <!-- ══════════ BULAN 4 ══════════ -->
  <div class="month-block visible" data-month="4" style="--month-color: var(--m4)">
    <div class="month-header">
      <div class="month-number">4</div>
      <div class="month-info">
        <div class="month-label">Bulan Keempat · Negosiasi</div>
        <div class="month-title">Negosiasi & Siapkan Dokumen</div>
        <div class="month-sub">Follow up buyer, negosiasi harga, susun kontrak</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-4">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-4">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w4-1">
      <div class="week-header" onclick="toggleWeek('w4-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Follow Up & Negosiasi Buyer</span>
        <span class="week-count" id="wc-w4-1">0/3</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Follow up semua buyer yang sudah terima sampel</div>
            <div class="task-detail">Follow up via WhatsApp / email max 7 hari setelah sampel tiba. Tanya feedback & tawaran harga awal (quotation).</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Hitung & kirim Proforma Invoice (PI) ke buyer serius</div>
            <div class="task-detail">PI berisi: harga/unit, total, Incoterms (FOB/CIF), payment terms, validity, port of loading & destination.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Verifikasi reputasi buyer (due diligence)</div>
            <div class="task-detail">Cek di Google, minta CR Number (Commercial Registration Saudi), atau konfirmasi via KBRI/ITPC Jeddah sebelum deal.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w4-2">
      <div class="week-header" onclick="toggleWeek('w4-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Kontrak & Sistem Pembayaran</span>
        <span class="week-count" id="wc-w4-2">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Tandatangani Sales Contract / Purchase Order</div>
            <div class="task-detail">Kontrak harus mencakup: spesifikasi produk, quantity, harga, incoterms, payment terms, delivery schedule, penalti.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Minta DP 30–50% atau setup L/C dari buyer</div>
            <div class="task-detail">Untuk order pertama: minta down payment. Untuk order >$10.000: minta Irrevocable L/C At Sight dari bank Saudi.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Urus izin tambahan jika produk masuk kategori khusus</div>
            <div class="task-detail">Pangan olahan: Sertifikat Kesehatan dari Badan Karantina. Kosmetik/farmasi: SFDA registration (importir Saudi yang urus).</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Hubungi Freight Forwarder untuk booking space & estimasi biaya</div>
            <div class="task-detail">Minta quotation dari min. 2 forwarder (bandingkan). Tanyakan: transit time, port Jeddah/Dammam, biaya THC & DO.</div>
          </div>
          <span class="task-badge badge-logistik">Logistik</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">📝</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 4</div>
        <div class="ms-text">PO / kontrak signed + DP sudah masuk rekening</div>
      </div>
    </div>
  </div>

  <div class="month-divider"></div>

  <!-- ══════════ BULAN 5 ══════════ -->
  <div class="month-block visible" data-month="5" style="--month-color: var(--m5)">
    <div class="month-header">
      <div class="month-number">5</div>
      <div class="month-info">
        <div class="month-label">Bulan Kelima · Produksi</div>
        <div class="month-title">Produksi & Persiapan Dokumen</div>
        <div class="month-sub">Produksi barang & siapkan semua dokumen ekspor</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-5">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-5">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w5-1">
      <div class="week-header" onclick="toggleWeek('w5-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Produksi & Quality Control</span>
        <span class="week-count" id="wc-w5-1">0/3</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Produksi batch ekspor sesuai spesifikasi kontrak</div>
            <div class="task-detail">Pastikan bahan baku 100% halal, tidak ada kontaminasi. Dokumentasi seluruh proses produksi (foto/video) untuk audit.</div>
          </div>
          <span class="task-badge badge-halal">Halal</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Quality Control: cek masa kadaluarsa & standar kemasan</div>
            <div class="task-detail">Saudi Customs reject barang jika masa kadaluarsa <50% sisa. Hitung: jika umur produk 12 bln, harus min. 6 bln sisa saat tiba.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Packing & labeling sesuai standar ekspor</div>
            <div class="task-detail">Label Arab harus benar. Gunakan stretch wrap, palet kayu fumigasi (ISPM 15), dan pastikan berat sesuai packing list.</div>
          </div>
          <span class="task-badge badge-logistik">Logistik</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w5-2">
      <div class="week-header" onclick="toggleWeek('w5-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Siapkan Semua Dokumen Ekspor</span>
        <span class="week-count" id="wc-w5-2">0/5</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Buat Commercial Invoice & Packing List final</div>
            <div class="task-detail">Invoice wajib ada: HS Code, unit price, total FOB value, payment terms, tanda tangan & stempel perusahaan.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Urus Certificate of Origin (SKA/COO) di Dinas Perdagangan</div>
            <div class="task-detail">Untuk tarif preferensial ASEAN-GCC. Bawa: Invoice, Packing List, bukti produksi lokal. Proses 1–3 hari, biaya ~Rp150rb.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Urus Sertifikat Kesehatan / Phytosanitary (pangan/pertanian)</div>
            <div class="task-detail">Diterbitkan Badan Karantina Pertanian (BARANTAN). Waktu proses 3–7 hari. Produk akan diperiksa fisik sebelum ekspor.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Ajukan PEB (Pemberitahuan Ekspor Barang) ke Bea Cukai</div>
            <div class="task-detail">Ajukan via CEISA minimal 1 hari sebelum loading. Lampirkan: Invoice, Packing List, COO, dan izin produk terkait.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Legalisasi dokumen di Kedutaan Saudi (jika first shipment)</div>
            <div class="task-detail">Kedubes Saudi di Jakarta (Jl. MT Haryono). Bawa: Halal Cert, COO, Invoice asli. Biaya & waktu tergantung jenis dokumen.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">📦</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 5</div>
        <div class="ms-text">Barang siap kirim + semua dokumen lengkap & tersertifikasi</div>
      </div>
    </div>
  </div>

  <div class="month-divider"></div>

  <!-- ══════════ BULAN 6 ══════════ -->
  <div class="month-block visible" data-month="6" style="--month-color: var(--m6)">
    <div class="month-header">
      <div class="month-number">6</div>
      <div class="month-info">
        <div class="month-label">Bulan Keenam · Eksekusi 🚀</div>
        <div class="month-title">First Shipment & Repeat Order</div>
        <div class="month-sub">Hari yang ditunggu — barang berangkat ke Saudi!</div>
      </div>
      <div class="month-progress">
        <div class="mp-ring" id="ring-6">
          <svg viewBox="0 0 36 36"><circle class="bg" cx="18" cy="18" r="16"/><circle class="fill" cx="18" cy="18" r="16"/></svg>
          <span class="pct-label" id="pct-6">0%</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w6-1">
      <div class="week-header" onclick="toggleWeek('w6-1')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 1–2</span>
        <span class="week-title">Pengiriman & Monitoring</span>
        <span class="week-count" id="wc-w6-1">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Serahkan barang ke freight forwarder & booking container</div>
            <div class="task-detail">Minta forwarder booking container 20ft/40ft sesuai volume. Pelabuhan tujuan: Jeddah Islamic Port atau King Abdul Aziz Port (Dammam).</div>
          </div>
          <span class="task-badge badge-logistik">Logistik</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Terima Bill of Lading (B/L) dari pelayaran</div>
            <div class="task-detail">B/L adalah bukti kepemilikan kargo. Kirimkan ke buyer Saudi (original atau telex release tergantung payment terms).</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Kirim semua dokumen asli ke buyer Saudi via DHL/FedEx</div>
            <div class="task-detail">Dokumen: B/L original, Invoice, Packing List, COO, Halal Cert, Health Cert. Wajib sebelum kapal tiba agar buyer bisa clearance.</div>
          </div>
          <span class="task-badge badge-wajib">Wajib</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Monitor tracking pengiriman hingga tiba di Jeddah/Dammam</div>
            <div class="task-detail">Transit time laut Indonesia–Jeddah: 15–25 hari. Update buyer secara proaktif setiap ada info dari pelayaran.</div>
          </div>
          <span class="task-badge badge-logistik">Logistik</span>
        </div>
      </div>
    </div>

    <div class="week-section" id="w6-2">
      <div class="week-header" onclick="toggleWeek('w6-2')">
        <div class="week-dot"></div>
        <span class="week-label">Mgg 3–4</span>
        <span class="week-title">Pembayaran, Evaluasi & Scale Up</span>
        <span class="week-count" id="wc-w6-2">0/4</span>
        <span class="week-chevron">▾</span>
      </div>
      <div class="week-body">
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Konfirmasi penerimaan barang & tagih pelunasan pembayaran</div>
            <div class="task-detail">Setelah buyer konfirmasi barang tiba OK, tagih sisa pembayaran (jika sistem DP 50%). Simpan semua bukti transfer.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Minta feedback & testimoni dari buyer</div>
            <div class="task-detail">Feedback buyer Saudi sangat berharga untuk perbaikan produk & kemasan. Ini juga bahan untuk marketing ke buyer lain.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Ajukan restitusi PPN 0% ke KPP (jika sudah PKP)</div>
            <div class="task-detail">Ekspor bebas PPN. Klaim restitusi dengan bukti: PEB, B/L, Invoice. Proses 1–3 bulan tapi ini uang Anda kembali!</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
        <div class="task-item" onclick="toggleTask(this)">
          <div class="task-check"><span class="task-tick">✓</span></div>
          <div class="task-content">
            <div class="task-name">Negosiasi repeat order & jadwal pengiriman rutin</div>
            <div class="task-detail">Tawarkan diskon volume untuk kontrak rutin (monthly/quarterly). Ini kunci membangun bisnis ekspor yang stabil jangka panjang.</div>
          </div>
          <span class="task-badge badge-bisnis">Bisnis</span>
        </div>
      </div>
    </div>

    <div class="milestone">
      <span class="ms-icon">🚀</span>
      <div class="ms-content">
        <div class="ms-label">Target akhir Bulan 6</div>
        <div class="ms-text">First shipment delivered ✓ Pembayaran lunas ✓ Repeat order in process</div>
      </div>
    </div>
  </div>

  <!-- Done Banner -->
  <div class="done-banner" id="done-banner">
    <h2>🎉 Alhamdulillah! Semua Selesai!</h2>
    <p>MasyaAllah — Anda siap menjadi eksportir Indonesia ke Arab Saudi. Bismillah! 🌙</p>
  </div>

  <button class="reset-btn" onclick="resetAll()">↺ Reset Semua Checklist</button>

</main>

<script>
const MONTHS = [1,2,3,4,5,6];
const WEEK_IDS = ['w1-1','w1-2','w2-1','w2-2','w3-1','w3-2','w4-1','w4-2','w5-1','w5-2','w6-1','w6-2'];

function toggleWeek(id) {
  const el = document.getElementById(id);
  el.classList.toggle('open');
}

function toggleTask(el) {
  el.classList.toggle('done');
  updateAll();
}

function updateAll() {
  let totalDone = 0, totalAll = 0;

  MONTHS.forEach(m => {
    const block = document.querySelector(`[data-month="${m}"]`);
    const all = block.querySelectorAll('.task-item');
    const done = block.querySelectorAll('.task-item.done');
    const pct = all.length ? Math.round((done.length / all.length) * 100) : 0;
    totalDone += done.length;
    totalAll += all.length;

    // ring
    const circumference = 100.5;
    const offset = circumference - (pct / 100) * circumference;
    const fillCircle = document.querySelector(`#ring-${m} .fill`);
    if (fillCircle) fillCircle.style.strokeDashoffset = offset;
    const pctLabel = document.getElementById(`pct-${m}`);
    if (pctLabel) pctLabel.textContent = pct + '%';
  });

  // Week counts
  WEEK_IDS.forEach(wid => {
    const sec = document.getElementById(wid);
    if (!sec) return;
    const all = sec.querySelectorAll('.task-item').length;
    const done = sec.querySelectorAll('.task-item.done').length;
    const el = document.getElementById('wc-' + wid);
    if (el) el.textContent = done + '/' + all;
  });

  // Global
  const pct = totalAll ? Math.round((totalDone / totalAll) * 100) : 0;
  document.getElementById('gp-fill').style.width = pct + '%';
  document.getElementById('gp-pct').textContent = pct + '%';
  document.getElementById('sum-done').textContent = totalDone;
  document.getElementById('sum-total').textContent = totalAll;
  document.getElementById('sum-pct').textContent = pct + '%';

  // Done banner
  const banner = document.getElementById('done-banner');
  banner.classList.toggle('show', totalDone === totalAll && totalAll > 0);
}

function showPhase(phase) {
  document.querySelectorAll('.phase-tab').forEach(t => t.classList.remove('active'));
  event.target.classList.add('active');

  document.querySelectorAll('.month-block').forEach(b => {
    if (phase === 'all' || b.dataset.month === phase) {
      b.classList.add('visible');
    } else {
      b.classList.remove('visible');
    }
  });
}

function resetAll() {
  document.querySelectorAll('.task-item').forEach(t => t.classList.remove('done'));
  updateAll();
}

// Init
updateAll();
// Open first week of each month by default
['w1-1','w2-1','w3-1','w4-1','w5-1','w6-1'].forEach(id => {
  const el = document.getElementById(id);
  if (el) el.classList.add('open');
});
</script>
</body>
</html>
