# SOP Publish Artikel Insights — Artha Karya Digital

## Alur standar (setelah automation draft)

1. Automation Senin 09:00 WITA → draft SEO lengkap + 3 image brief
2. Owner review (setuju / revisi)
3. Setelah setuju, bilang ke Grok: **Publish artikel [slug]**
4. Grok akan:
   - Generate 3 gambar Imagine
   - Buat folder `id/insights/[slug]/`
   - Tulis `index.html` dari template + konten
   - Update `id/insights/index.html` (listing)
   - Update `sitemap.xml`
   - Siapkan path gambar di `assets/img/insights/[slug]/`
   - **Commit & push ke GitHub** `ekakoel/arthakarya-website`
5. Hostinger Git auto-deploy (jika sudah dihubungkan)
6. Search Console → Request indexing URL baru

## Checklist SEO sebelum publish

- [ ] Title 50–60 karakter
- [ ] Meta 140–155 karakter
- [ ] 1 H1, jawaban di pembuka
- [ ] ≥2 internal link (1 ke layanan)
- [ ] 3 gambar + alt text
- [ ] Schema Article
- [ ] Canonical & sitemap
- [ ] Tidak ada hype / jaminan ranking
