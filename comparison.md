# So sánh DevOps vs Traditional + Workflow

**Sinh viên:** Hoàng Thạch An — DTC235180001

## 1. Bảng so sánh

| Tiêu chí | Traditional (Truyền thống) | DevOps |
|---|---|---|
| Deploy | Thủ công, copy file qua FTP/USB | Tự động qua CI/CD pipeline |
| Thời gian release | Vài ngày/tuần, dễ lỗi sót file | Vài phút sau mỗi `git push` |
| Kiểm thử | Test tay cuối vòng đời | Test + Lighthouse audit tự động mỗi commit |
| Phối hợp | Dev ném code cho Ops deploy | Dev + Ops chung pipeline, chung trách nhiệm |
| Rollback | Khó, phải tìm bản cũ thủ công | Dễ, revert commit → pipeline deploy lại |
| Giám sát | Ít, khi lỗi mới kiểm tra | Actions log + Pages + Lighthouse report mỗi lần push |

## 2. Workflow DevOps trong Lab 1

```
Code (index.html / about.html / contact.html + avatar)
  → git push origin main
  → GitHub Actions: deploy.yml (build + upload artifact + deploy-pages)
  → GitHub Pages Live (https://thachrc.github.io/devops-lab1-portfolio/)
  → lighthouse.yml audit Performance / Accessibility / Best Practices / SEO
  → Xem kết quả ở tab Actions
```

Sửa code → push → pipeline chạy lại → web update sau 1-2 phút, không cần deploy tay.
