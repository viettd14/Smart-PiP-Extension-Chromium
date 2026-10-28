<div align="center">

# Smart PiP

**Xem nhiều video. Trong một cửa sổ nổi. Không gián đoạn công việc.**

Tiện ích Picture-in-Picture dành cho trình duyệt Chromium, hỗ trợ gom nhiều video vào một giao diện (Multi-View).

[![Latest Release](https://img.shields.io/github/v/release/viettd14/Smart-PiP-Extension-Chromium?label=Stable%20Release)](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest)
![Platform](https://img.shields.io/badge/Platform-Chromium-4285F4)
![Manifest](https://img.shields.io/badge/Manifest-V3-6A5ACD)

[**Tải phiên bản mới nhất**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest) · [**Xem lịch sử phát hành**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases) · [**Báo lỗi / Đề xuất**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/issues)

</div>

---

## ✨ Giới thiệu

**Smart PiP** giúp bạn theo dõi video trong một cửa sổ nổi khi chuyển tab hoặc làm việc với ứng dụng khác. Thay vì chỉ xem một video như Picture-in-Picture thông thường, **Multi-PiP** trên phiên bản **v2.0.0** cho phép tập hợp tối đa **4 video tương thích** vào một bố cục Multi-View.

Phù hợp khi bạn muốn theo dõi nhiều luồng nội dung mà không phải liên tục chuyển qua lại giữa các tab.

## 🚀 Tính năng nổi bật

| | Tính năng | Mô tả |
|---|---|---|
| 🪟 | **Cửa sổ nổi** | Giữ video hiển thị trong khi làm việc ở tab khác. |
| 🎬 | **Multi-PiP (tối đa 4 video)** | Gom các video tương thích vào cùng một cửa sổ Multi-View. |
| 🖱️ | **Thao tác nhanh** | Thêm video từ các tab tương thích bằng biểu tượng extension. |
| ⏯️ | **Điều khiển phát** | Play/Pause, tua, âm lượng và tốc độ phát; mức hỗ trợ tùy video. |
| 💬 | **Phụ đề** | Ưu tiên hiển thị phụ đề trên YouTube và một số trình phát HTML5 tương thích. |
| 🔄 | **Kiểm tra cập nhật** | Kiểm tra phiên bản mới thông qua GitHub Releases. |

## 📥 Cài đặt

1. Mở [**Releases**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest) và tải **gói cài đặt ZIP của Smart PiP**, nếu được đính kèm trong phần **Assets**.
2. Giải nén vào một thư mục cố định trên máy.
3. Mở trang quản lý extension của trình duyệt:
   - Chrome: `chrome://extensions`
   - Edge: `edge://extensions`
   - Brave: `brave://extensions`
4. Bật **Developer mode** → chọn **Load unpacked** → chọn thư mục chứa `manifest.json`.
5. Ghim Smart PiP lên thanh công cụ để sử dụng thuận tiện hơn.

> **Lưu ý:** Các mục **Source code (zip)** / **Source code (tar.gz)** do GitHub tự tạo không nhất thiết là gói cài đặt extension. Hãy chọn file cài đặt được đính kèm riêng trong Assets (nếu có).

## 🎮 Cách sử dụng

1. Mở trang video tương thích (ưu tiên YouTube).
2. Nhấn biểu tượng **Smart PiP** để bắt đầu xem trong cửa sổ nổi.
3. Mở thêm video ở tab khác rồi nhấn biểu tượng Smart PiP để đưa vào Multi-View.
4. Sử dụng các điều khiển có sẵn để quản lý từng video.

## 🧩 Multi-PiP hoạt động thế nào?

Smart PiP sử dụng **Document Picture-in-Picture** để hiển thị giao diện nổi. Với nhiều video, extension kết hợp cơ chế truyền luồng video từ các tab tương thích vào giao diện Multi-View. Vì vậy, đây **không phải bốn cửa sổ native PiP độc lập**.

**Giới hạn hiện tại:** Chất lượng hình ảnh có thể phụ thuộc vào nguồn video, trình duyệt và khả năng truyền luồng; một số trang sử dụng DRM hoặc trình phát đặc biệt có thể không hỗ trợ đầy đủ. Khi đóng tab nguồn, video tương ứng có thể ngừng phát. Một số tính năng phụ đề và điều khiển phụ thuộc vào website.

## 🛠️ Phản hồi & phát triển

Gặp lỗi hoặc có ý tưởng cải tiến? Hãy tạo một [**Issue**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/issues) và mô tả trình duyệt, website video, các bước tái hiện và kết quả mong muốn.

Thông tin thay đổi theo từng phiên bản được cập nhật tại [**GitHub Releases**](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases).

---

<div align="center">

**Smart PiP** · Developed by **Việt Trần**

</div>
