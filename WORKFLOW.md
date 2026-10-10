# Sistem Sinkron: Automation ↔ GitHub ↔ Website

## Arsitektur

```
[Grok Automation] → draft SEO + images
        ↓
[Owner approve] → "Publish artikel [slug]"
        ↓
[Grok] tulis HTML + commit ke GitHub (ekakoel/arthakarya-website)
        ↓
[Hostinger Git Deployment] auto-pull branch main
        ↓
[Live] arthakaryadigital.com
        ↓
[Search Console] request indexing
```

## Komponen

| Komponen | Fungsi |
|----------|--------|
| Repo `ekakoel/arthakarya-website` | Source of truth kode website |
| Hostinger Git | Deploy otomatis dari `main` |
| Automation AKD Insights Artikel SEO 2 Mingguan | Draft artikel + 3 image brief |
| Automation AKD Publish Artikel Package | Package publish setelah approve |
| Skill `seo-content-akd` | Standar SEO artikel |
| Drive `Website/rebuild/` | Working copy lokal Grok |

## Alur artikel (rutin)

1. Senin 09:00 WITA — automation kirim draft
2. Owner review
3. Owner: **Publish artikel [slug]**
4. Grok: HTML + sitemap + listing + push GitHub
5. Hostinger deploy otomatis
6. Owner: Search Console → indexing

## Setup Hostinger Git (sekali)

1. hPanel → Advanced → Git
2. Create / connect repository
3. URL: `https://github.com/ekakoel/arthakarya-website.git`
4. Branch: `main`
5. Install path: folder domain (`public_html`)
6. Deploy

## Catatan gambar

File binary (webp/png) di-upload via File Manager atau commit lokal. Automation menyiapkan path + alt text.
