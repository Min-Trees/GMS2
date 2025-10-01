# 📝 Hướng Dẫn Tạo Lesson Mới cho Khóa Học GameMaker Studio 2

## 🎯 Mục đích
File này hướng dẫn cách tạo lesson mới phù hợp với giao diện và cấu trúc của hệ thống học tập GameMaker Studio 2 dành cho học sinh cấp 2.

## 📋 Cấu trúc file lesson

### 1. Phần đầu file (HTML head)
```html
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>[Tên Lesson] - Buổi [X]</title>
  <link rel="stylesheet" href="style.css" />
  <script type="module">
    import mermaid from "https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs";
    mermaid.initialize({
      startOnLoad: true,
      theme: "dark",
      themeVariables: {
        primaryColor: "#111827",
        primaryBorderColor: "#22d3ee",
        primaryTextColor: "#e5e7eb",
        lineColor: "#22d3ee",
        secondaryColor: "#0b1222",
        tertiaryColor: "#0b1222",
        fontFamily: "system-ui, Segoe UI, Roboto, Helvetica, Arial",
        fontSize: "16px",
        labelBackground: "#1f2937",
        labelTextColor: "#e5e7eb",
        nodeBorder: "#22d3ee",
        clusterBackground: "#0b1222",
        clusterBorder: "#22d3ee"
      }
    });
  </script>
</head>
```

### 2. Phần body chính
```html
<body>
  <main class="wrap">
    <nav class="breadcrumb">
      <a href="index.html">🏠 Trang chủ</a> > <span>Buổi [X]</span>
    </nav>
    <h1>[Emoji] [Tên Lesson] - Buổi [X]</h1>

    <!-- Nội dung chính -->
    
    <nav class="lesson-nav">
      <a href="lesson[X-1].html" class="nav-link">← Buổi [X-1]: [Tên buổi trước]</a>
      <a href="lesson[X+1].html" class="nav-link">Buổi [X+1]: [Tên buổi sau] →</a>
    </nav>
  </main>
</body>
</html>
```

## 🎨 Nguyên tắc thiết kế

### 1. Sử dụng emoji
- Mỗi section bắt đầu với emoji phù hợp
- Emoji trong sơ đồ Mermaid để thu hút học sinh
- Ví dụ: 🎮, 🛠️, 📘, 🔍, ⚙️, 🎯, 💡, 🚀

### 2. Cấu trúc section
```html
<section class="card">
  <h2>[Số]) [Emoji] [Tiêu đề]</h2>
  <p>[Mô tả ngắn gọn]</p>
  
  <!-- Sơ đồ Mermaid (nếu cần) -->
  <div class="mermaid">
flowchart TD
  A["🎯 Node 1"] --> B["🎮 Node 2"]
  B --> C["✅ Node 3"]
      </div>
  
  <!-- Nội dung chi tiết -->
  <h3>[Tiêu đề phụ]</h3>
  <ul class="tips">
    <li><strong>[Từ khóa]</strong>: [Mô tả chi tiết]</li>
    <li><strong>[Từ khóa]</strong>: [Mô tả chi tiết]</li>
  </ul>
  
  <!-- Code examples -->
  <pre><code>[Mã GML hoặc code khác]</code></pre>
  
  <p class="note">📌 Nếu sơ đồ không hiện, kiểm tra mạng (cần tải Mermaid) hoặc thử trình duyệt khác.</p>
</section>
```

### 3. Sơ đồ Mermaid
- **Luôn đặt text trong ngoặc kép**: `A["Text"]` thay vì `A[Text]`
- **Sử dụng emoji**: Làm sơ đồ sinh động và dễ hiểu
- **Cấu trúc rõ ràng**: Tránh chồng chéo, sử dụng flowchart TD hoặc LR
- **Thêm ghi chú**: Luôn có dòng note về Mermaid

### 4. Nội dung phù hợp học sinh cấp 2
- **Ngôn ngữ đơn giản**: Tránh thuật ngữ phức tạp
- **Ví dụ cụ thể**: Luôn có ví dụ thực tế
- **Giải thích từng bước**: Chia nhỏ thành các bước dễ hiểu
- **Mẹo thực tế**: Thêm phần "Mẹo tránh lỗi" nếu cần

## 📝 Các section bắt buộc

### 1. Section tóm tắt cuối bài
```html
<section class="card">
  <h2>[Số]) 🎯 Tóm tắt buổi học</h2>
  <p>Trong buổi học này, chúng ta đã học được:</p>
  <ul class="tips">
    <li>✅ [Điểm 1]</li>
    <li>✅ [Điểm 2]</li>
    <li>✅ [Điểm 3]</li>
  </ul>
  <p><strong>Bài tập về nhà:</strong> [Nhiệm vụ thực hành cụ thể]</p>
</section>
```

### 2. Navigation
```html
<nav class="lesson-nav">
  <a href="lesson[X-1].html" class="nav-link">← Buổi [X-1]: [Tên]</a>
  <a href="lesson[X+1].html" class="nav-link">Buổi [X+1]: [Tên] →</a>
</nav>
```

## 🚫 Những điều cần tránh

1. **Không sử dụng placeholder hình ảnh**: `<em>[Hình minh họa: ...]</em>`
2. **Không sử dụng sơ đồ Mermaid phức tạp**: Giữ đơn giản, dễ hiểu
3. **Không sử dụng thuật ngữ khó**: Giải thích bằng ngôn ngữ đơn giản
4. **Không quên ghi chú Mermaid**: Luôn có dòng note
5. **Không sử dụng text trong ngoặc vuông**: `A[Text]` → `A["Text"]`

## ✅ Checklist trước khi hoàn thành

- [ ] Có breadcrumb navigation
- [ ] Có section tóm tắt cuối bài
- [ ] Có navigation giữa các lesson
- [ ] Tất cả sơ đồ Mermaid có text trong ngoặc kép
- [ ] Có ghi chú Mermaid cho mỗi sơ đồ
- [ ] Không có placeholder hình ảnh
- [ ] Ngôn ngữ phù hợp học sinh cấp 2
- [ ] Có ví dụ thực tế và code cụ thể
- [ ] Có bài tập về nhà

## 🎯 Ví dụ về sơ đồ Mermaid tốt

```html
<div class="mermaid">
flowchart TD
  A["🚀 Bắt đầu game"] --> B["⚙️ Khởi tạo đối tượng"]
  B --> C["🔄 Vòng lặp chính"]
  C --> D{"❓ Có va chạm?"}
  D -->|Có| E["💥 Xử lý va chạm"]
  D -->|Không| F["🎮 Tiếp tục game"]
  E --> C
  F --> C
</div>
```

## 📚 Tham khảo các lesson hiện có
- `lesson1.html`: Ôn tập kiến thức cơ bản
- `lesson2.html`: Lý thuyết GML và thực hành  
- `lesson3.html`: Game bắn súng từ trên xuống

Hãy tham khảo cấu trúc và phong cách của các file này để tạo lesson mới phù hợp!
