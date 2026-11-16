Nama Proyek: Portal Resmi & Ekosistem Digital Kesultanan Bima Dompu

Versi: 1.0

Inisiator: King Cahyadi, S.Kom

Tech Stack Utama: Next.js 15+ (App Router), TypeScript, Tailwind CSS, Prisma/Drizzle ORM, PostgreSQL

1.1 Latar Belakang & Tujuan
Membangun platform digital terpusat (single source of truth) yang merepresentasikan identitas budaya, sejarah, informasi resmi, dan ekosistem unit usaha/komunitas Kesultanan Bima Dompu (termasuk integrasi Dompu News, Cahyadi's Course, Dompu Lens, Dompu Tech Solution, Dompu Law Firm, serta agenda acara seperti Royal Games Festival).

1.2 Target Pengguna (User Personas)
Masyarakat Umum & Warga Bima-Dompu: Mengakses berita terkini, sejarah kesultanan, jadwal acara/turnamen, dan layanan publik.

Peserta Event & Turnamen: Melakukan registrasi lomba (Catur, Domino, Remi, Uno, Senam Sehat) dan memantau bagan pertandingan (bracket / leaderboard).

Mitra & Sponsor (B2B/Instansi): Mengakses informasi Open Sponsorship, mengunduh proposal kemitraan, dan mengajukan kerja sama.

Admin / Pengelola Konten (Tim Kerajaan & Redaksi): Mengelola publikasi berita, memperbarui jadwal event, memverifikasi peserta, dan mengatur aset branding.

1.3 Fitur Utama & Persyaratan Fungsional
A. Portal Utama & Profil Kesultanan (Public Facing)
Landing Page Eksekutif: Hero section dengan sambutan resmi Baginda King Cahyadi, S.Kom, sorotan acara terdekat, dan navigasi cepat.

Sejarah & Budaya (Mbojo - Dompu): Halaman arsip digital yang memuat nilai budaya, tradisi, dan filosofi Nggahi Rawi Pahu / Maja Labo Dahu.

Direktori Ekosistem & Unit Usaha: Etalase terintegrasi untuk unit di bawah naungan ekosistem (Dompu News, Cahyadi's Course, Dompu Lens, Dompu Law Firm & Partner, Dompu Tech Solution, Dompu Land, Dompu Kontraktor & Interior).

B. Sistem Manajemen Event & Turnamen (Royal Games & Community)
Katalog Event & Pendaftaran Online: Formulir pendaftaran peserta turnamen dengan validasi nomor WhatsApp dan pemilihan cabang lomba.

Live Bracket & Klasemen: Tampilan jadwal pertandingan dan hasil skor secara real-time (menggunakan Next.js Server Actions & revalidation).

Portal Open Sponsorship: Halaman khusus bagi calon sponsor untuk melihat paket kemitraan (Gold, Silver, Bronze) dan mengajukan inquiry langsung.

C. Integrasi Berita & Media (Dompu News & Cahaya Dis TV)
News Feed & Artikel: Publikasi berita daerah dengan optimasi SEO dinamis (generateMetadata), kategori berita, dan fitur share ke media sosial.

Galeri Dokumentasi (Dompu Lens): Galeri foto resolusi tinggi menggunakan next/image dengan lazy loading dan lightbox viewer.

D. Dashboard Admin (Protected Route)
Autentikasi Berbasis Role (RBAC): Menggunakan Auth.js (NextAuth v5) dengan pembagian hak akses (SUPER_ADMIN, EDITOR_BERITA, PANITIA_EVENT).

CMS & Manajemen Data: CRUD berita, manajemen pendaftar lomba, dan ekspor data peserta ke format CSV/Excel.

1.4 Persyaratan Non-Fungsional & Arsitektur Next.js
Performa (Core Web Vitals): Target skor Lighthouse > 95. Memanfaatkan React Server Components (RSC) secara default dan Incremental Static Regeneration (ISR) untuk halaman berita/profil.

Keamanan: Proteksi CSRF pada Server Actions, validasi skema input menggunakan Zod, serta rate-limiting pada formulir pendaftaran publik.

Responsivitas: Desain mobile-first mengingat mayoritas akses pengguna di Bima-Dompu berasal dari perangkat seluler.