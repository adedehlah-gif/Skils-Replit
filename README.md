# Replit Pro UI/UX Skill Pack

Paket ini berisi skill dan rules untuk membantu Replit Agent membuat UI/UX yang profesional, konsisten, responsif, dan dapat digunakan.

## Isi paket

```text
replit-pro-ui-ux-skills/
├── .agents/
│   └── skills/
│       └── pro-ui-ux/
│           └── SKILL.md
├── AGENTS.md
└── README.md
```

## Cara memasang pada satu project

1. Ekstrak ZIP.
2. Salin folder `.agents/skills/pro-ui-ux/` ke root project Replit.
3. Salin `AGENTS.md` ke root project (gabungkan dengan file aturan yang sudah ada; jangan menimpa aturan penting).
4. Di Replit Agent, minta: **“Baca `AGENTS.md` dan `.agents/skills/pro-ui-ux/SKILL.md` terlebih dahulu, lalu ikuti aturan tersebut untuk semua pekerjaan UI/UX di project ini.”**
5. Uji dengan meminta Agent membuat atau memperbaiki satu halaman dan periksa apakah ia mengikuti checklist.

## Agar tersedia lintas project

Skill di dalam folder project berlaku untuk project tempat skill itu dipasang. Untuk menggunakannya lintas project, buka Replit **Workspace Settings → Customization** (nama menu bisa berubah), lalu:
- Tambahkan instruksi global yang mewajibkan Agent membaca/mengikuti skill UI/UX ini pada setiap pekerjaan antarmuka.
- Unggah/tambahkan skill melalui fitur Skills yang tersedia di workspace.
- Jika tersedia, pasang skill pada level workspace/account, bukan hanya satu project.

Replit mendokumentasikan bahwa project-level skills disimpan di `/.agents/skills`, sementara Custom Instructions adalah mekanisme untuk aturan yang selalu aktif. Ketersediaan Custom Instructions dapat bergantung pada paket/workspace Replit. Skill yang hanya diunggah ke satu project **tidak otomatis** menjamin semua project lain membacanya.

## Instruksi global siap salin

> Untuk setiap project dan setiap tugas yang membuat, mengubah, memperbaiki, atau meninjau UI/UX, sebelum menulis kode baca dan ikuti skill `pro-ui-ux` (`.agents/skills/pro-ui-ux/SKILL.md`). Jika skill tersedia di workspace, gunakan skill tersebut. Jika tidak tersedia di project, minta saya memasangnya atau gunakan aturan UI/UX profesional yang sama: hierarchy yang jelas, design tokens konsisten, responsif untuk mobile/tablet/desktop, aksesibilitas, kontrol yang berfungsi, state loading/empty/error/success, dan verifikasi hasil. Jangan mengklaim skill telah dibaca jika belum.

## Arah desain

Skill terinspirasi dari referensi dashboard E-Learning yang diberikan: latar putih bersih, navigasi samping yang jelas, banner teal, aksen coral dan kuning, kartu ringkas, visualisasi progres, tipografi yang mudah dibaca, dan layout yang rapi. Prinsipnya diadaptasi sesuai kebutuhan produk—bukan menyalin gambar secara buta.

## Catatan

Skill adalah instruksi untuk Agent, bukan mekanisme penguncian teknis. Untuk memastikan penerapannya lintas project, pasang di tingkat workspace/account bila fitur tersebut tersedia dan verifikasi perilaku Agent pada project baru.
