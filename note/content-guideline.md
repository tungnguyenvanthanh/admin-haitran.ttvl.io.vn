# 🚚 Công ty TH Express

**TH Express** là đơn vị chuyển phát nhanh hoạt động dựa trên nền tảng kinh nghiệm thực tế, quy trình vận hành rõ ràng và sự am hiểu sâu sắc về ngành **logistics – vận chuyển liên tỉnh và nước ngoài**.

Chúng tôi là **đối tác tin cậy** của cá nhân và doanh nghiệp, đồng hành trong việc gửi hàng **nhanh chóng – an toàn – đúng hẹn**.

---

## 📞 Thông tin liên hệ

- **Hotline / Zalo:** 0948.659.123 – 0931.452.225  
- **Email:** thanhhoa.thexpress@gmail.com  
- **Địa chỉ:** Số 14, đường Thị Tứ, Hoằng Phú, Hoằng Hóa, Thanh Hóa

---

## Mục tiêu tài liệu

Tài liệu này hướng dẫn cách viết nội dung và ví dụ UI (HTML snippet) để người viết content và front-end developer triển khai giao diện nhất quán, responsive và accessible theo template sử dụng Bootstrap 5.

- Ngôn ngữ: tiếng Việt (nội dung hiển thị) — giữ phong cách ngắn gọn, rõ ràng.
- Kiểu: các component nhỏ (list, button, quote, CTA, heading, gallery) kèm lớp CSS và attribute gợi ý.

---

## Nguyên tắc chung (Bootstrap 5)

- Layout: dùng `container` / `container-fluid`, `row`, `col-*`.
- Ảnh: luôn thêm `class="img-fluid"` và `loading="lazy"` cho performance.
- Typography: sử dụng `lead`, `fw-*`, `text-*`.
- Spacing: dùng utility `mb-*`, `mt-*`, `py-*`, `px-*`.
- Buttons/CTA: dùng `default-btn` cho phù hợp với lớp hiện tại của template.
- Icons trang trí: thêm `aria-hidden="true"` và không dùng thay cho nội dung chính.
- Accessibility: CTA nếu chỉ có icon cần `aria-label`, các region có `aria-label` khi cần.

---

## Component ví dụ

Dưới đây các ví dụ có thể copy trực tiếp vào trang, tùy chỉnh text, đường dẫn (`href`) và classes theo theme.

### 1) Danh sách kiểm tra (Checklist)

```html
<ul class="check-list mb-20 wow fade-in-bottom" data-wow-delay="100ms">
    <li><i class="fa-solid fa-check" aria-hidden="true"></i> Quản lý vận chuyển hàng hóa hiệu quả</li>
    <li><i class="fa-solid fa-check" aria-hidden="true"></i> Tùy chọn vận chuyển chuyên biệt cho hàng dễ vỡ và thực phẩm</li>
    <li><i class="fa-solid fa-check" aria-hidden="true"></i> Theo dõi hành trình thời gian thực với cập nhật</li>
</ul>
```

Ghi chú: thay text bằng tiếng Việt cho nhất quán; giữ icon `aria-hidden`.

---

### 2) Nút hành động (Button / Link)

```html
<a href="/lien-he" class="default-btn wow fade-in-bottom" data-wow-delay="200ms" aria-label="Liên hệ TH Express">Liên hệ</a>
```

Ghi chú: nếu dùng chỉ icon, thêm `aria-label` rõ ràng.

---

### 3) Trích dẫn (Quote)

```html
<blockquote class="quote-style wow fade-in-bottom" data-wow-delay="150ms">
    <i class="fa-sharp fa-regular fa-quote-right" aria-hidden="true"></i>
    Thông tin về kiện hàng quan trọng không kém việc<br>giao nhận kiện hàng đúng thời gian…
    <cite>- TH Express</cite>
</blockquote>
```

Biến thể (boxed):

```html
<blockquote class="quote-box p-20 bg-light border-start border-3 border-primary wow fade-in-bottom" data-wow-delay="150ms">
    <i class="fa-sharp fa-regular fa-quote-right" aria-hidden="true"></i>
    Thông tin về kiện hàng quan trọng không kém việc<br>giao nhận kiện hàng đúng thời gian…
    <cite class="d-block mt-2">- TH Express</cite>
</blockquote>
```

Ghi chú: thêm thẻ `<i>` icon và CSS cho `quote-style`/`quote-box` trong stylesheet nếu cần.

---

### 4) CTA (Call To Action) - Block nổi bật

```html
<div class="card bg-danger text-white mt-5 shadow-sm">
    <div class="card-body text-center">
        <h3 class="mb-3 text-white">Liên hệ TH Express ngay hôm nay</h3>
        <p class="mb-3">Gửi hàng đi Mỹ an toàn – nhanh chóng – đúng quy định chưa bao giờ dễ dàng đến thế.</p>
        <p class="fw-semibold mb-3">Hotline / Zalo:
            <a class="text-white" href="tel:0948659123">0948 659 123</a> –
            <a class="text-white" href="tel:0931452225">0931 452 225</a>
        </p>
        <a href="/lien-he" class="btn btn-light default-btn" role="button" aria-label="Liên hệ TH Express">Liên hệ</a>
    </div>
</div>
```

Ghi chú: kiểm tra tương phản màu khi dùng `bg-danger` + `text-white`.

---

### 5) Tiêu đề mục con (h3)

```html
<!-- Tiêu đề đơn giản -->
<h3 class="mb-3">Future of Transportation</h3>

<!-- Tiêu đề kèm icon -->
<h3 class="mb-3"><i class="fa-solid fa-truck-fast me-2" aria-hidden="true"></i>Future of Transportation</h3>

<!-- Tiêu đề kèm badge -->
<h3 class="mb-3">Future of Transportation <span class="badge bg-primary ms-2">New</span></h3>
```

Ghi chú: dùng `me-2` để cách icon và thêm `aria-hidden` cho icon trang trí.

---

### 6) Gallery ảnh

```html
<section class="mb-3">
    <h4 class="fw-semibold mb-3 text-center">Hình ảnh thực tế</h4>
    <ul class="gallery list-unstyled d-flex flex-wrap justify-content-center" aria-label="Gallery hình ảnh thực tế">
        <li class="m-2">
            <img src="/images/img1.jpg" alt="Xe giao nhận TH Express tại kho" class="img-fluid" loading="lazy">
        </li>
        <!-- Thêm ảnh khác tương tự -->
    </ul>
</section>
```

Ghi chú: mọi ảnh quan trọng cần `alt` rõ ràng; sử dụng `width`/`height` sắp xếp ratio nếu cần.

---

## Accessibility & Performance (nhắc lại)

- Icon trang trí: `aria-hidden="true"`.
- CTA chỉ icon: thêm `aria-label` hoặc visible label cho screen readers.
- Ảnh: `alt` mô tả, `loading="lazy"`, tối ưu kích thước và định dạng (WebP/AVIF khi có thể).
- Kiểm tra độ tương phản màu theo WCAG (4.5:1 cho text nhỏ).

---

## Hướng dẫn viết nội dung cho UI

- Văn phong: ngắn gọn, chủ động, hướng hành động (ví dụ: "Đặt ngay", "Liên hệ ngay").
- Giữ nội dung button ngắn (1–3 từ) và rõ ràng.
- Dùng bullet/ul cho danh sách lợi ích hoặc hướng dẫn từng bước.
- Sử dụng tiêu đề `h2` / `h3` để chia section, giữ hierarchy rõ ràng cho SEO và a11y.

---

## Lưu ý kỹ thuật cho developer

- Các class `wow`, `fade-in-bottom`, `data-wow-delay` là animation helper — kiểm tra performance và cho phép tắt trên reduced-motion preference.
- Nếu template dùng `default-btn`, đảm bảo map thành `btn`/`btn-*` của Bootstrap hoặc style tương đương.
- Kiểm tra responsive trên `sm`, `md`, `lg` cho các block CTA và gallery.

---

## Mẫu nhanh để copy (tổng hợp)

```html
<!-- Checklist -->
<ul class="check-list mb-20">
  <li><i class="fa-solid fa-check" aria-hidden="true"></i> Quản lý vận chuyển nhanh chóng</li>
  <li><i class="fa-solid fa-check" aria-hidden="true"></i> Theo dõi hành trình thời gian thực</li>
</ul>

<!-- Quote -->
<blockquote class="quote-box p-3 bg-light border-start border-3 border-primary">
  <i class="fa-sharp fa-regular fa-quote-right" aria-hidden="true"></i>
  Thông tin kiện hàng là yếu tố quan trọng để giao nhận thành công.
  <cite class="d-block mt-2">- TH Express</cite>
</blockquote>

<!-- CTA -->
<div class="card bg-danger text-white mt-4">
  <div class="card-body text-center">
    <h3>Liên hệ TH Express ngay</h3>
    <p>Gửi hàng an toàn và nhanh chóng.</p>
    <a href="/lien-he" class="btn btn-light" aria-label="Liên hệ TH Express">Liên hệ</a>
  </div>
</div>
```

---

Nếu cần, tôi có thể tách phần CSS gợi ý (các lớp custom như `quote-box`, `check-list`, `default-btn`) ra thành một đoạn CSS mẫu để developer bổ sung vào stylesheet chung.