# DevOps Lab 1 — Portfolio CI/CD với GitHub Actions & GitHub Pages

**Họ tên:** Hoàng Thạch An
**MSSV:** DTC235180001
**Repo:** https://github.com/ThachRC/devops-lab1-portfolio
**Website:** https://thachrc.github.io/devops-lab1-portfolio/

## Mô tả
Lab 01: Trải nghiệm CI/CD với GitHub Actions và GitHub Pages.
Push code lên nhánh `main` → pipeline `deploy.yml` chạy → tự động deploy lên GitHub Pages.
Workflow `lighthouse.yml` audit Performance, Accessibility, Best Practices, SEO tự động mỗi lần push.

## Cấu trúc
- `index.html` — Trang chủ portfolio (có avatar, navigation)
- `about.html` — Giới thiệu bản thân
- `contact.html` — Liên hệ
- `assets/avatar.jpg` — Ảnh đại diện
- `.github/workflows/deploy.yml` — Pipeline deploy Pages
- `.github/workflows/lighthouse.yml` — Lighthouse CI audit
- `comparison.md` — Bảng so sánh DevOps vs Traditional + Workflow

## Cách chạy pipeline
1. `git push origin main`
2. Mở tab Actions trên GitHub xem `Deploy to GitHub Pages` chạy xanh
3. Mở URL `*.github.io` kiểm tra web đã update
