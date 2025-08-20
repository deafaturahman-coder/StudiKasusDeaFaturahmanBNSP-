# StudiKasusDeaFaturahmanBNSP-
dasbor strategi pemasaran digital interaktif Rengginang “West Java Youth” dengan fokus pada storytelling, audiens Gen Z, konten kreatif, iklan berbayar, KPI, kolaborasi KOL, PR digital, serta pemanfaatan AI. Disusun oleh Dea Faturahman untuk sertifikasi BNSP Digital Marketing Dispora Jabar.
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dasbor Strategi Pemasaran Digital - West Java Youth</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Sand -->
    <!-- Application Structure Plan: The application is designed as a single-page dashboard with a fixed sidebar navigation for seamless exploration. This structure was chosen over a linear, report-style layout to allow users to jump directly to sections of interest (e.g., Budget, KPIs, Audience) and interact with the data. The flow is as follows: 1) Overview/Welcome, 2) Core Strategy Pillars, 3) Detailed exploration via sidebar (Audience, Content, Ads, KPIs, etc.). This non-linear approach enhances usability by empowering the user to explore the strategy based on their own priorities, making the complex information more digestible and engaging. -->
    <!-- Visualization & Content Choices: 
        - Report Info: Budget Allocation (Rp 1,000,000) -> Goal: Inform -> Viz: Interactive Doughnut Chart (Chart.js) -> Interaction: Hover to see budget per campaign -> Justification: Provides a quick, clear visual breakdown of spending priorities.
        - Report Info: Target KPIs (Impressions, ER, CTR) -> Goal: Inform/Compare -> Viz: Dynamic Bar Chart (Chart.js) -> Interaction: Buttons to switch between KPI views -> Justification: Allows for easy comparison of target metrics and focuses on key performance goals.
        - Report Info: Target Audience Segments -> Goal: Organize -> Viz: Interactive Cards (HTML/CSS/JS) -> Interaction: Click to reveal details of each segment -> Justification: Presents audience data in a clean, organized manner without overwhelming the user initially. Also added a dedicated Gen Z section.
        - Report Info: Content Strategy (Carousel Examples) -> Goal: Organize/Inform -> Viz: Tabbed Interface (HTML/CSS/JS) -> Interaction: Click tabs to view different carousel content plans -> Justification: Efficiently displays multiple detailed examples in a compact space.
        - Report Info: AI Tools -> Goal: Organize -> Viz: Grid Layout with Icons (HTML/CSS) -> Interaction: Static display -> Justification: A simple grid is sufficient to list tools and their functions clearly.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #FDF8F0;
            color: #4A4A4A;
        }
        .sidebar-link {
            transition: all 0.3s ease;
            border-left: 3px solid transparent;
        }
        .sidebar-link:hover, .sidebar-link.active {
            background-color: #F4EADE;
            color: #AF8F6F;
            border-left-color: #AF8F6F;
        }
        .card {
            background-color: #FFFFFF;
            border-radius: 0.75rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -2px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.07), 0 4px 6px -4px rgba(0, 0, 0, 0.07);
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .btn-primary {
            background-color: #AF8F6F;
            color: #FFFFFF;
            transition: background-color 0.3s ease;
        }
        .btn-primary:hover {
            background-color: #8E735B;
        }
        .btn-secondary {
            background-color: #F4EADE;
            color: #AF8F6F;
            transition: background-color 0.3s ease;
        }
        .btn-secondary.active {
            background-color: #AF8F6F;
            color: #FFFFFF;
        }
    </style>
</head>
<body class="flex min-h-screen">
    <aside class="w-64 bg-white shadow-md fixed h-full hidden lg:block">
        <div class="p-6">
            <h1 class="text-2xl font-bold text-[#AF8F6F]">West Java Youth</h1>
            <p class="text-sm text-gray-500">Dasbor Strategi Digital</p>
        </div>
        <nav class="mt-6">
            <a href="#ringkasan" class="sidebar-link active block py-3 px-6 text-gray-700 font-medium">Ringkasan</a>
            <a href="#audiens" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Target Audiens</a>
            <a href="#genz" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Positioning Gen Z</a>
            <a href="#konten" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Strategi Konten</a>
            <a href="#iklan" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Rencana Iklan</a>
            <a href="#kpi" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Target Kinerja (KPI)</a>
            <a href="#kolaborasi" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Kolaborasi KOL</a>
            <a href="#evaluasi" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Evaluasi Campaign</a>
            <a href="#pr" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Manajemen PR</a>
            <a href="#ai" class="sidebar-link block py-3 px-6 text-gray-700 font-medium">Pemanfaatan AI</a>
        </nav>
    </aside>

    <main class="flex-1 lg:ml-64 p-4 sm:p-6 md:p-8">
        <div class="max-w-7xl mx-auto">
            
            <section id="ringkasan" class="mb-12">
                <div class="card p-6">
                    <h2 class="text-3xl font-bold text-[#8E735B] mb-4">Strategi Pemasaran Digital Rengginang "West Java Youth"</h2>
                    <p class="text-gray-600 mb-6">Selamat datang di dasbor strategi interaktif untuk "West Java Youth". Di sini, kita akan membedah rencana pemasaran digital dengan anggaran Rp 1.000.000. Tujuannya adalah menjembatani warisan kuliner lokal dengan gaya hidup modern melalui *storytelling* otentik, optimalisasi organik, dan investasi iklan yang presisi. Gunakan navigasi di samping untuk menjelajahi setiap bagian dari strategi ini.</p>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
                        <div class="bg-[#F4EADE] p-4 rounded-lg">
                            <h3 class="text-lg font-bold text-[#AF8F6F]">Storytelling Otentik</h3>
                            <p class="text-sm text-gray-600 mt-1">Membangun narasi merek yang kuat dan terhubung secara emosional dengan audiens.</p>
                        </div>
                        <div class="bg-[#F4EADE] p-4 rounded-lg">
                            <h3 class="text-lg font-bold text-[#AF8F6F]">Optimalisasi Cerdas</h3>
                            <p class="text-sm text-gray-600 mt-1">Memaksimalkan visibilitas organik melalui SEO di media sosial dan marketplace.</p>
                        </div>
                        <div class="bg-[#F4EADE] p-4 rounded-lg">
                            <h3 class="text-lg font-bold text-[#AF8F6F]">Investasi Presisi</h3>
                            <p class="text-sm text-gray-600 mt-1">Menggunakan iklan berbayar untuk mendapatkan data dan mengakselerasi pertumbuhan.</p>
                        </div>
                    </div>
                </div>
            </section>

            <section id="audiens" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Memahami Target Audiens Kita</h2>
                <p class="text-gray-600 mb-6">Analisis mendalam terhadap pasar dan psikografi konsumen menunjukkan bahwa produk camilan tradisional seperti *rengginang* memiliki daya tarik yang luas. Namun, dengan keterbatasan anggaran, upaya untuk menjangkau semua segmen pasar dapat menjadi kontraproduktif. Oleh karena itu, strategi difokuskan untuk menargetkan segmen yang paling berpotensi dan relevan.</p>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="card p-6 text-center cursor-pointer" onclick="toggleAudienceDetails(this)">
                        <div class="text-4xl mb-3">🎯</div>
                        <h3 class="text-xl font-bold text-[#8E735B]">Audiens Primer (Gen Z)</h3>
                        <p class="text-gray-500 font-medium">Usia: 18-24 tahun</p>
                        <div class="audience-details hidden mt-4 text-left text-sm text-gray-600">
                            <p><strong>Demografi:</strong> Usia 18-24 tahun, laki-laki dan perempuan, berdomisili di perkotaan dan sub-urban di seluruh Indonesia, khususnya Jawa Barat. Status ekonomi: mahasiswa, *first jobber*, atau pelajar dengan uang saku dan kemampuan belanja online.</p>
                            <p class="mt-2"><strong>Psikografi:</strong> *Digital-native*, aktif di media sosial (TikTok, Instagram, Twitter), menyukai tren, hobi *hangout*, *gaming*, atau *streaming*. Menghargai produk estetik, punya cerita, peduli kesehatan, bangga produk lokal, menyukai otentisitas dengan sentuhan modern, peduli lingkungan.</p>
                            <p class="mt-2"><strong>Hobi:</strong> Ngemil saat menonton film/series, bermain game online (*mabar*), membuat konten media sosial, mencari kafe/tempat nongkrong *aesthetic*.</p>
                        </div>
                    </div>
                    <div class="card p-6 text-center cursor-pointer" onclick="toggleAudienceDetails(this)">
                        <div class="text-4xl mb-3">👩‍👧‍👦</div>
                        <h3 class="text-xl font-bold text-[#8E735B]">Audiens Sekunder</h3>
                        <p class="text-gray-500 font-medium">Ibu Muda Perkotaan (25-45 thn)</p>
                         <div class="audience-details hidden mt-4 text-left text-sm text-gray-600">
                            <p><strong>Fokus Utama:</strong> Mencari camilan berkualitas, praktis, dan sehat untuk keluarga. Aktif di Facebook & WhatsApp.</p>
                            <p class="mt-2"><strong>Strategi:</strong> Menekankan kualitas bahan baku, proses higienis, dan kepraktisan produk sebagai camilan keluarga.</p>
                        </div>
                    </div>
                    <div class="card p-6 text-center cursor-pointer" onclick="toggleAudienceDetails(this)">
                        <div class="text-4xl mb-3">✈️</div>
                        <h3 class="text-xl font-bold text-[#8E735B]">Audiens Tersier</h3>
                        <p class="text-gray-500 font-medium">Wisatawan Kuliner</p>
                         <div class="audience-details hidden mt-4 text-left text-sm text-gray-600">
                            <p><strong>Fokus Utama:</strong> Mencari oleh-oleh khas Bandung yang unik dan otentik.</p>
                            <p class="mt-2"><strong>Strategi:</strong> Optimalisasi SEO lokal (#oleholehbandung) dan kolaborasi dengan akun-akun travel/kuliner lokal.</p>
                        </div>
                    </div>
                </div>
            </section>

            <section id="genz" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Positioning & Relevansi untuk Gen Z: "The OG Snack with a Vibe!"</h2>
                <p class="text-gray-600 mb-6">Untuk menarik Gen Z, **West Java Youth** diposisikan sebagai "The OG Snack with a Vibe!" — camilan otentik dengan nuansa kekinian yang sesuai gaya hidup mereka. Tagline **"Kriuk Tradisi, Rasa Generasi!"** memperkuat pesan ini.</p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="card p-6">
                        <h3 class="text-xl font-bold text-[#8E735B] mb-3">Makna Tagline untuk Gen Z</h3>
                        <ul class="list-disc list-inside text-gray-600 space-y-2">
                            <li>**Kriuk Tradisi:** Menunjukkan warisan kuliner Sunda, otentik, kaya makna budaya.</li>
                            <li>**Rasa Generasi:** Dihadirkan ulang dengan gaya baru yang *relate* dengan generasi sekarang.</li>
                        </ul>
                    </div>
                    <div class="card p-6">
                        <h3 class="text-xl font-bold text-[#8E735B] mb-3">Key Messages untuk Gen Z</h3>
                        <ul class="list-disc list-inside text-gray-600 space-y-2">
                            <li>**Taste:** "Rengginang bukan cuma asin. Ini kriuk otentik + vibe kekinian yang bikin nagih!"</li>
                            <li>**Aesthetic:** "Snack lokal yang estetik buat feed IG/TikTok kamu. Gak cuma enak, tapi juga fotogenik!"</li>
                            <li>**Lifestyle:** "Temen nugas, mabar, atau binge-watching. Rengginang yang *upgrade*, buat kamu yang gak mau ribet!"</li>
                            <li>**Gifting:** "Oleh-oleh Bandung yang anti-mainstream. Bikin temen-temen kamu nge-tag dan penasaran!"</li>
                        </ul>
                    </div>
                </div>
            </section>

            <section id="konten" class="mb-12">
                 <h2 class="text-2xl font-bold mb-4">Rencana Konten & Peningkatan Engagement</h2>
                 <p class="text-gray-600 mb-6">Konten adalah jantung dari strategi organik kita. Tujuannya bukan hanya promosi, tapi membangun kepercayaan dan komunitas melalui cerita yang otentik. Berikut adalah contoh pilar konten dan desain visual dalam format *carousel* yang bisa diadaptasi untuk Instagram dan TikTok.</p>
                <div class="card p-6">
                    <div class="flex border-b mb-4">
                        <button class="content-tab active py-2 px-4 font-medium text-[#AF8F6F] border-b-2 border-[#AF8F6F]" onclick="switchContentTab(event, 'testimoni')">Testimoni Pelanggan</button>
                        <button class="content-tab py-2 px-4 font-medium text-gray-500" onclick="switchContentTab(event, 'bts')">Behind The Scenes</button>
                    </div>
                    <div id="testimoni" class="content-panel">
                        <h3 class="text-lg font-bold mb-2">Carousel: "Jangan Percaya Kami, Percaya Mereka!"</h3>
                        <p class="text-sm text-gray-600 mb-4">Tujuan: Membangun bukti sosial (*social proof*) dan kredibilitas merek melalui ulasan otentik dari pelanggan.</p>
                        <div class="grid grid-cols-2 md:grid-cols-5 gap-3">
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 1 (Cover):</b> "Testimoni Nyata Pelanggan Kami!"</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 2-3:</b> Tangkapan layar testimoni dari WhatsApp atau DM, dengan visual produk.</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 4:</b> Narasi singkat tentang perasaan pelanggan setelah mencoba produk.</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 5 (CTA):</b> "Sudah coba juga? Yuk, *share* pengalamanmu!"</div>
                        </div>
                    </div>
                    <div id="bts" class="content-panel hidden">
                        <h3 class="text-lg font-bold mb-2">Carousel: "Proses di Balik Renyahnya Rengginang Kami"</h3>
                        <p class="text-sm text-gray-600 mb-4">Tujuan: Meningkatkan transparansi dan membangun koneksi emosional dengan menunjukkan proses pembuatan yang otentik.</p>
                        <div class="grid grid-cols-2 md:grid-cols-5 gap-3">
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 1 (Cover):</b> "Yuk, Lihat Proses Kami Bikin Rengginang!"</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 2:</b> Visual pemilihan bahan baku dari petani lokal.</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 3:</b> Foto proses penjemuran atau penggorengan tradisional.</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 4:</b> Proses pengemasan higienis dan modern.</div>
                            <div class="bg-gray-100 p-3 rounded-lg text-center text-xs"><b>Slide 5 (CTA):</b> "Semua kami lakukan untuk memberikan yang terbaik. Pesan sekarang!"</div>
                        </div>
                    </div>
                     <h3 class="text-lg font-bold mt-6 mb-2">Jenis Konten (1 bulan, 3-4 posting/minggu)</h3>
                    <ul class="list-disc list-inside text-gray-600 space-y-1">
                        <li>**Edukasi:** Fakta unik Rengginang & cerita budaya Jawa Barat.</li>
                        <li>**Engagement:** Polling, quiz “Team Pedas atau Asin?”, challenge makan rengginang tanpa pecah.</li>
                        <li>**Promosi Produk:** Highlight varian rasa, testimoni pelanggan.</li>
                        <li>**Lifestyle:** Konten estetik “Ngemil rengginang saat kerja/Netflixan.”</li>
                        <li>**User Generated Content (UGC):** Repost dari konsumen.</li>
                    </ul>
                </div>
            </section>

            <section id="iklan" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Alokasi Anggaran Iklan Berbayar (Rp 1.000.000)</h2>
                <p class="text-gray-600 mb-6">Dengan anggaran terbatas, alokasi iklan akan difokuskan pada platform yang paling sering digunakan target pasar (Instagram, TikTok, Shopee). Iklan berbayar memastikan konten bisa menjangkau audiens lebih luas dibanding organik saja.</p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div class="card p-6">
                        <h3 class="font-bold text-lg mb-4">Breakdown Kampanye</h3>
                        <div class="space-y-4">
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="font-medium">Kampanye 1: Instagram & Facebook Ads</span>
                                    <span class="font-bold text-[#AF8F6F]">Rp 500.000</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-2.5">
                                    <div class="bg-[#AF8F6F] h-2.5 rounded-full" style="width: 50%"></div>
                                </div>
                                <p class="text-xs text-gray-500 mt-1">Target: 18–35 tahun, Bandung + Jabodetabek. Objective: traffic ke Shopee/Tokopedia. Format: Carousel + Video pendek.</p>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="font-medium">Kampanye 2: TikTok Ads</span>
                                    <span class="font-bold text-[#AF8F6F]">Rp 300.000</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-2.5">
                                    <div class="bg-[#8E735B] h-2.5 rounded-full" style="width: 30%"></div>
                                </div>
                                <p class="text-xs text-gray-500 mt-1">Target: Gen Z & Milenial. Objective: Awareness + Engagement. Format: In-Feed Ads (konten snack kekinian).</p>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="font-medium">Kampanye 3: Shopee Ads</span>
                                    <span class="font-bold text-[#AF8F6F]">Rp 200.000</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-2.5">
                                    <div class="bg-[#C8A27D] h-2.5 rounded-full" style="width: 20%"></div>
                                </div>
                                <p class="text-xs text-gray-500 mt-1">Keyword: “Cemilan tradisional”, “Rengginang Bandung”, “Snack lokal enak”.</p>
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="chart-container">
                            <canvas id="budgetChart"></canvas>
                        </div>
                    </div>
                </div>
            </section>
            
            <section id="kpi" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Target Kinerja Utama (KPI)</h2>
                <p class="text-gray-600 mb-6">Fokus kita adalah pada metrik yang benar-benar menunjukkan pertumbuhan bisnis. Grafik di bawah ini menunjukkan target awal kita untuk 30 hari pertama. Gunakan tombol untuk melihat detail setiap KPI.</p>
                <div class="card p-6">
                    <div class="flex justify-center mb-4 space-x-2">
                        <button id="btn-followers" class="btn-secondary active px-4 py-2 rounded-full text-sm font-medium" onclick="updateKpiChart('followers')">Followers Baru</button>
                        <button id="btn-engagement" class="btn-secondary px-4 py-2 rounded-full text-sm font-medium" onclick="updateKpiChart('engagement')">Engagement Rate</button>
                        <button id="btn-reach" class="btn-secondary px-4 py-2 rounded-full text-sm font-medium" onclick="updateKpiChart('reach')">Organic Reach</button>
                        <button id="btn-views" class="btn-secondary px-4 py-2 rounded-full text-sm font-medium" onclick="updateKpiChart('views')">Video Views</button>
                        <button id="btn-orders" class="btn-secondary px-4 py-2 rounded-full text-sm font-medium" onclick="updateKpiChart('orders')">Jumlah Order</button>
                    </div>
                    <div class="chart-container h-80 md:h-96">
                        <canvas id="kpiChart"></canvas>
                    </div>
                </div>
            </section>

            <section id="kolaborasi" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Strategi Kolaborasi Influencer (KOL)</h2>
                <p class="text-gray-600 mb-6">Dengan budget terbatas, kita akan fokus pada *nano* dan *micro influencer* yang memiliki audiens loyal dan *engagement* tinggi. Tujuannya bukan penjualan langsung, melainkan untuk menghasilkan *User-Generated Content* (UGC) otentik yang bisa kita gunakan kembali sebagai materi promosi.</p>
                <div class="card p-6 grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
                     <div>
                        <h3 class="font-bold text-lg text-[#8E735B]">Tipe Influencer</h3>
                        <p class="text-2xl my-2">👤</p>
                        <p class="text-gray-600">Nano/Micro Influencer<br>(10K - 50K Followers)</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg text-[#8E735B]">Tujuan Utama</h3>
                        <p class="text-2xl my-2">📸</p>
                        <p class="text-gray-600">Mendapatkan UGC Otentik & Meningkatkan Kredibilitas</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg text-[#8E735B]">Model Kerjasama</h3>
                        <p class="text-2xl my-2">🤝</p>
                        <p class="text-gray-600">Prioritas Barter Produk, Opsi Afiliasi/Komisi</p>
                    </div>
                     <div class="md:col-span-3">
                        <p class="text-gray-600 mt-4 text-sm">Target: 2 micro influencer kuliner Bandung (IG/TikTok). Format: Review + storytelling. KPI: 1.000–5.000 views per konten, minimal 50 DM/order traffic masuk.</p>
                    </div>
                </div>
            </section>

             <section id="evaluasi" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Kerangka Evaluasi & Analisis Performa Kampanye</h2>
                <p class="text-gray-600 mb-6">Evaluasi adalah langkah krusial untuk memastikan bahwa investasi yang dilakukan efektif dan dapat menjadi dasar untuk perbaikan berkelanjutan. Proses evaluasi akan dilakukan secara praktis dan rutin.</p>
                <div class="card p-6">
                    <h3 class="font-bold text-lg mb-4">Metrik yang Diukur</h3>
                    <ul class="list-disc list-inside text-gray-600 space-y-1">
                        <li>Reach, engagement, CTR, jumlah order, cost per purchase.</li>
                        <li>**Tools:** Meta Ads Manager, TikTok Analytics, Shopee/Tokopedia Seller Center.</li>
                    </ul>
                    <h3 class="font-bold text-lg mt-6 mb-4">Timeline Evaluasi</h3>
                    <ul class="list-disc list-inside text-gray-600 space-y-1">
                        <li>Minggu ke-1 & ke-2 → evaluasi iklan (pause iklan tidak efektif).</li>
                        <li>Minggu ke-4 → laporan akhir & strategi perbaikan.</li>
                    </ul>
                    <h3 class="font-bold text-lg mt-6 mb-4">Templat Laporan Performa Sederhana (per bulan)</h3>
                    <div class="overflow-x-auto">
                        <table class="min-w-full bg-white border border-gray-200 rounded-lg">
                            <thead>
                                <tr class="bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider">
                                    <th class="py-3 px-4 border-b">KPI</th>
                                    <th class="py-3 px-4 border-b">Target</th>
                                    <th class="py-3 px-4 border-b">Hasil Aktual</th>
                                    <th class="py-3 px-4 border-b">Analisis & Catatan</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr class="text-gray-700">
                                    <td class="py-2 px-4 border-b">Engagement Rate</td>
                                    <td class="py-2 px-4 border-b">>1.94%</td>
                                    <td class="py-2 px-4 border-b"></td>
                                    <td class="py-2 px-4 border-b">Mengidentifikasi jenis konten yang berkinerja terbaik untuk direplikasi.</td>
                                </tr>
                                <tr class="bg-gray-50 text-gray-700">
                                    <td class="py-2 px-4 border-b">Total Impressions</td>
                                    <td class="py-2 px-4 border-b">100.000</td>
                                    <td class="py-2 px-4 border-b"></td>
                                    <td class="py-2 px-4 border-b">Menilai jangkauan kampanye organik dan berbayar.</td>
                                </tr>
                                <tr class="text-gray-700">
                                    <td class="py-2 px-4 border-b">CTR (Iklan)</td>
                                    <td class="py-2 px-4 border-b">>1%</td>
                                    <td class="py-2 px-4 border-b"></td>
                                    <td class="py-2 px-4 border-b">Mengukur efektivitas visual dan *copywriting* iklan.</td>
                                </tr>
                                <tr class="bg-gray-50 text-gray-700">
                                    <td class="py-2 px-4 border-b">Penjualan (Konversi)</td>
                                    <td class="py-2 px-4 border-b"></td>
                                    <td class="py-2 px-4 border-b"></td>
                                    <td class="py-2 px-4 border-b">Menilai dampak langsung kampanye terhadap pendapatan.</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </section>

             <section id="pr" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Manajemen Public Relations Digital</h2>
                <p class="text-gray-600 mb-6">Untuk UMKM, PR adalah upaya sistematis untuk membangun citra positif dan hubungan baik dengan publik melalui media digital. PR tidak harus mahal; implementasinya dapat dilakukan secara praktis.</p>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="card p-6 text-center">
                        <h3 class="font-bold text-lg text-[#8E735B]">Publikasi Digital</h3>
                        <p class="text-2xl my-2">📰</p>
                        <p class="text-gray-600 text-sm">Ciptakan "berita" tentang merek (giveaway, varian baru) di media lokal (BandungNow, InfoBDG).</p>
                    </div>
                    <div class="card p-6 text-center">
                        <h3 class="font-bold text-lg text-[#8E735B]">Keterlibatan Komunitas</h3>
                        <p class="text-2xl my-2">💬</p>
                        <p class="text-gray-600 text-sm">Aktif di komunitas kuliner online atau grup lokal di Facebook dan WhatsApp.</p>
                    </div>
                    <div class="card p-6 text-center">
                        <h3 class="font-bold text-lg text-[#8E735B]">Manajemen Citra</h3>
                        <p class="text-2xl my-2">👍</p>
                        <p class="text-gray-600 text-sm">Respon cepat dan profesional terhadap komentar/ulasan (positif & negatif).</p>
                    </div>
                    <div class="md:col-span-3">
                         <h3 class="font-bold text-lg mt-6 mb-2">Inisiatif CSR (Contoh)</h3>
                        <p class="text-gray-600 text-sm">Donasi rengginang untuk panti asuhan, didokumentasikan sebagai konten *storytelling* untuk meningkatkan *brand trust*.</p>
                    </div>
                </div>
            </section>


            <section id="ai" class="mb-12">
                <h2 class="text-2xl font-bold mb-4">Mengoptimalkan Kinerja dengan AI</h2>
                <p class="text-gray-600 mb-6">Kecerdasan Buatan (AI) berfungsi sebagai asisten virtual yang membantu mengotomatisasi tugas-tugas rutin, menganalisis data, dan meningkatkan efisiensi operasional dengan budget terbatas.</p>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4">
                    <div class="card p-4 text-center">
                        <h3 class="font-bold">ChatGPT / Google Gemini</h3>
                        <p class="text-sm text-gray-500">Ide Konten & Copywriting</p>
                    </div>
                    <div class="card p-4 text-center">
                        <h3 class="font-bold">Canva AI</h3>
                        <p class="text-sm text-gray-500">Desain Visual Cepat</p>
                    </div>
                    <div class="card p-4 text-center">
                        <h3 class="font-bold">Quillbot</h3>
                        <p class="text-sm text-gray-500">Penyempurnaan Teks</p>
                    </div>
                    <div class="card p-4 text-center">
                        <h3 class="font-bold">Hootsuite</h3>
                        <p class="text-sm text-gray-500">Penjadwalan Postingan</p>
                    </div>
                    <div class="card p-4 text-center">
                        <h3 class="font-bold">Google Looker Studio</h3>
                        <p class="text-sm text-gray-500">Analisis Data Kampanye</p>
                    </div>
                </div>
            </section>
        </div>
    </main>

    <script>
        // Global variable to store the currently active KPI type
        let currentKpiType = 'followers'; // Initialize with the default active KPI

        document.addEventListener('DOMContentLoaded', function () {
            
            const budgetData = {
                labels: ['Instagram & Facebook Ads (Rp 500k)', 'TikTok Ads (Rp 300k)', 'Shopee Ads (Rp 200k)'],
                datasets: [{
                    data: [500000, 300000, 200000],
                    backgroundColor: ['#AF8F6F', '#8E735B', '#C8A27D'],
                    hoverBackgroundColor: ['#8E735B', '#5E453B', '#A68460'],
                    borderColor: '#FDF8F0',
                    borderWidth: 4,
                }]
            };
            const budgetCtx = document.getElementById('budgetChart').getContext('2d');
            new Chart(budgetCtx, {
                type: 'doughnut',
                data: budgetData,
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    cutout: '60%',
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                color: '#4A4A4A',
                                font: {
                                    family: "'Inter', sans-serif",
                                    size: 14
                                }
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed !== null) {
                                        label += new Intl.NumberFormat('id-ID', { style: 'currency', currency: 'IDR', minimumFractionDigits: 0 }).format(context.parsed);
                                    }
                                    return label;
                                }
                            }
                        }
                    }
                }
            });

            const kpiData = {
                followers: {
                    labels: ['Target Instagram', 'Target TikTok'],
                    datasets: [{
                        label: 'Followers Baru',
                        data: [500, 300],
                        backgroundColor: ['#AF8F6F', '#8E735B'],
                        borderColor: ['#8E735B', '#5E453B'],
                        borderWidth: 1,
                        barThickness: 50,
                    }]
                },
                engagement: {
                    labels: ['Target Engagement Rate'],
                    datasets: [{
                        label: 'Engagement Rate (%)',
                        data: [5],
                        backgroundColor: '#AF8F6F',
                        borderColor: '#8E735B',
                        borderWidth: 1,
                        barThickness: 50,
                    }]
                },
                reach: {
                    labels: ['Target Organic Reach'],
                    datasets: [{
                        label: 'Organic Reach (Akun)',
                        data: [10000],
                        backgroundColor: '#AF8F6F',
                        borderColor: '#8E735B',
                        borderWidth: 1,
                        barThickness: 50,
                    }]
                },
                views: {
                    labels: ['Target Video Views (TikTok)'],
                    datasets: [{
                        label: 'Video Views (≥10K)',
                        data: [10000],
                        backgroundColor: '#AF8F6F',
                        borderColor: '#8E735B',
                        borderWidth: 1,
                        barThickness: 50,
                    }]
                },
                orders: {
                    labels: ['Target Order Pertama'],
                    datasets: [{
                        label: 'Jumlah Order',
                        data: [100],
                        backgroundColor: '#AF8F6F',
                        borderColor: '#8E735B',
                        borderWidth: 1,
                        barThickness: 50,
                    }]
                }
            };

            const kpiCtx = document.getElementById('kpiChart').getContext('2d');
            window.kpiChart = new Chart(kpiCtx, {
                type: 'bar',
                data: kpiData.followers,
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        y: {
                            beginAtZero: true,
                            ticks: {
                                callback: function(value, index, values) {
                                    // Use currentKpiType to determine if it's a percentage
                                    if (currentKpiType === 'engagement') {
                                        return value + '%';
                                    }
                                    // For CTR, it's typically a percentage too (although CTR is not a button in the current setup)
                                    if (currentKpiType === 'ctr') {
                                        return value + '%';
                                    }
                                    return new Intl.NumberFormat('id-ID').format(value);
                                },
                                color: '#4A4A4A'
                            }
                        },
                        x: {
                            ticks: { color: '#4A4A4A' }
                        }
                    },
                    plugins: {
                        legend: { display: false },
                        tooltip: {
                             callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.y !== null) {
                                        // Use currentKpiType for tooltip formatting as well
                                        if (currentKpiType === 'engagement' || currentKpiType === 'ctr') {
                                            label += context.parsed.y + '%';
                                        } else {
                                           label += new Intl.NumberFormat('id-ID').format(context.parsed.y);
                                        }
                                    }
                                    return label;
                                }
                            }
                        }
                    }
                }
            });

            window.updateKpiChart = function(kpi) {
                currentKpiType = kpi; // Update the global variable
                kpiChart.data = kpiData[kpi];
                kpiChart.update();
                document.querySelectorAll('#kpi .btn-secondary').forEach(btn => btn.classList.remove('active'));
                document.getElementById(`btn-${kpi}`).classList.add('active');
            };

            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.sidebar-link');

            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.4
            };

            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        navLinks.forEach(link => {
                            link.classList.remove('active');
                            if (link.getAttribute('href').substring(1) === entry.target.id) {
                                link.classList.add('active');
                            }
                        });
                    }
                });
            }, observerOptions);

            sections.forEach(section => {
                observer.observe(section);
            });
            
            navLinks.forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });

        });

        function toggleAudienceDetails(element) {
            const details = element.querySelector('.audience-details');
            details.classList.toggle('hidden');
        }

        function switchContentTab(event, tabName) {
            document.querySelectorAll('.content-panel').forEach(panel => panel.classList.add('hidden'));
            document.getElementById(tabName).classList.remove('hidden');
            document.querySelectorAll('.content-tab').forEach(tab => tab.classList.remove('active', 'text-[#AF8F6F]', 'border-[#AF8F6F]'));
            document.querySelectorAll('.content-tab').forEach(tab => tab.classList.add('text-gray-500'));
            event.currentTarget.classList.add('active', 'text-[#AF8F6F]', 'border-[#AF8F6F]');
            event.currentTarget.classList.remove('text-gray-500');
        }

    </script>
</body>
</html>
