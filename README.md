<div align="center">

# 🎬 Smart PiP

### Multi-Video Picture-in-Picture for Chromium Browsers

**Xem tối đa 4 video cùng lúc trong một cửa sổ nổi — không cần chuyển qua lại giữa các tab.**

[![Version](https://img.shields.io/badge/version-v2.0.0-blue?style=flat-square)](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/tag/v2.0.0)
![Manifest V3](https://img.shields.io/badge/Manifest-V3-097969?style=flat-square)
![Platform](https://img.shields.io/badge/Chromium-Chrome%20%7C%20Edge%20%7C%20Brave-orange?style=flat-square)
[![Latest Release](https://img.shields.io/github/v/release/viettd14/Smart-PiP-Extension-Chromium?label=latest%20release&style=flat-square)](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest)

**[📥 Download latest release](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest)** · **[📋 Release notes](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases)** · **[🐛 Report an issue](https://github.com/viettd14/Smart-PiP-Extension-Chromium/issues)**

</div>

---

## ✨ Giới thiệu

**Smart PiP** là tiện ích mở rộng cho các trình duyệt dựa trên Chromium, giúp đưa video vào cửa sổ nổi **Picture-in-Picture** để vừa xem vừa làm việc. Phiên bản **v2.0.0** bổ sung **Multi-PiP**, cho phép gom tối đa **4 video tương thích** vào một giao diện Multi-View.

> **Demo giao diện:** Thêm ảnh chụp hoặc GIF thực tế vào `assets/demo-multipip.gif`, sau đó bỏ dấu chú thích ở dòng dưới để hiển thị.
>
> `![Smart PiP Multi-View Demo](assets/demo-multipip.gif)`

## 🚀 Tính năng

| Nhóm | Khả năng |
| --- | --- |
| 🪟 **Floating player** | Xem video trong cửa sổ nổi khi chuyển sang ứng dụng hoặc tab khác. |
| 🎞️ **Multi-PiP** | Gom tối đa 4 video từ các tab tương thích vào một cửa sổ Multi-View. |
| ⏯️ **Playback controls** | Play/Pause, tua ±10 giây và theo dõi tiến trình phát. |
| 🔊 **Audio controls** | Mute/Unmute, thay đổi âm lượng và tốc độ phát. |
| 💬 **Subtitles** | Ưu tiên duy trì phụ đề khi trình phát/website hỗ trợ. |
| ⚙️ **Player options** | Hỗ trợ lựa chọn chất lượng khi trình phát cho phép. |
| 🔔 **Update checker** | Kiểm tra phiên bản mới qua GitHub Releases trong **Options → Updates**. |

## 📦 Cài đặt

Hiện Smart PiP được cài bằng cách **Load unpacked** (không cần Chrome Web Store).

1. Mở trang **[Releases](https://github.com/viettd14/Smart-PiP-Extension-Chromium/releases/latest)**, tải **file ZIP bản cài đặt** nếu release có đính kèm file này. **Không sử dụng `Source code (zip)` tự động do GitHub tạo** thay cho bản cài đặt nếu repository chưa chứa mã nguồn tương ứng.
2. Giải nén vào một thư mục cố định; kiểm tra thư mục đó có file **`manifest.json`**.
3. Mở `chrome://extensions`, `edge://extensions` hoặc `brave://extensions`.
4. Bật **Developer mode** → **Load unpacked** → chọn thư mục chứa `manifest.json`.
5. Mở trang video tương thích, nhấn biểu tượng **Smart PiP** trên thanh công cụ.

> **Lưu ý tải xuống:** Nếu trang Releases hiện chưa có file ZIP cài đặt riêng trong **Assets**, cần bổ sung file ZIP extension v2.0.0 vào release. Mục `Source code (zip)` của GitHub chỉ đóng gói nội dung tại commit gắn tag.

### Nâng cấp

Sao lưu nếu có thay đổi cục bộ, đóng cửa sổ PiP, giải nén bản mới và chép đè đúng thư mục extension đã cài → truy cập trang `extensions` → nhấn **Reload**. Sau đó refresh lại các tab đang mở video.

## 🧭 Cách sử dụng Multi-PiP

1. Mở video đầu tiên trong tab tương thích, nhấn biểu tượng Smart PiP để khởi tạo cửa sổ nổi.
2. Mở những video tiếp theo trên tab khác, nhấn biểu tượng Smart PiP để thêm vào Multi-View (tối đa 4 video).
3. Điều khiển phát video trực tiếp trong giao diện nổi, tùy theo khả năng của từng trình phát.

### Multi-PiP hoạt động như thế nào?

Smart PiP dùng **Document Picture-in-Picture** để hiển thị giao diện nổi. Khi bổ sung video từ tab khác, extension dùng cơ chế **capture/stream và WebRTC** để truyền video vào Hub. Vì vậy, đây là **một cửa sổ PiP chứa nhiều luồng**, không phải bốn cửa sổ PiP độc lập.

```text
Tab video #1 ──────┐
Tab video #2 ──────┤
Tab video #3 ──────┼──► Multi-View Hub ──► Floating PiP Window
Tab video #4 ──────┘
```

## 🖥️ Trình duyệt tương thích

- Google Chrome
- Microsoft Edge
- Brave

Cần phiên bản trình duyệt hỗ trợ các API PiP liên quan. Hành vi có thể khác nhau giữa các phiên bản Chromium và website phát video.

## ⚠️ Giới hạn hiện tại

- Multi-PiP ưu tiên **YouTube và HTML5 video** tương thích; một số website có iframe đặc biệt hoặc DRM có thể không hoạt động.
- Luồng video bổ sung phải qua capture và WebRTC, vì vậy **chất lượng, độ trễ và mức sử dụng tài nguyên** có thể khác với video gốc.
- Phụ đề ở các video bổ sung phụ thuộc cách website render subtitle; không bảo đảm mọi subtitle được truyền đầy đủ.
- Nếu tab gốc giữ vai trò Host bị đóng, phiên PiP/Hub có thể bị ảnh hưởng; hiện chưa hỗ trợ chuyển Host liên tục mà không gián đoạn.
- Update checker **chỉ kiểm tra và dẫn đến phiên bản mới**, không tự cài đặt.

## ❓ FAQ

**Vì sao bấm extension mà không có gì xảy ra?**  
Trang hiện tại có thể chưa có video phù hợp, hoặc trình phát không cho phép extension truy cập.

**Có cần Share Tab thủ công không?**  
Không trong luồng sử dụng Multi-PiP đã hỗ trợ.

**Vì sao video thứ hai có thể kém nét hơn?**  
Vì các video bổ sung được truyền qua capture/WebRTC; chất lượng chịu tác động bởi đường truyền, tài nguyên máy và cách trình duyệt mã hóa luồng.

**Extension có tự nâng cấp không?**  
Chưa. Vào **Options → Updates** để kiểm tra phiên bản rồi nâng cấp thủ công.

## 🗺️ Hướng phát triển

Các hướng **đang xem xét**, chưa phải tính năng đã phát hành:

- Cải thiện độ nét và tính ổn định của các luồng video bổ sung.
- Nghiên cứu khả năng phục hồi/chuyển Host khi tab đầu bị đóng.
- Mở rộng khả năng tương thích với video HTML5 và phụ đề.
- Tối ưu trải nghiệm Multi-View và cơ chế cập nhật.

## 🐛 Phản hồi & hỗ trợ

Gặp lỗi hoặc có đề xuất? Hãy tạo [GitHub Issue](https://github.com/viettd14/Smart-PiP-Extension-Chromium/issues), kèm trình duyệt, phiên bản, website phát video và bước tái hiện (tránh chia sẻ dữ liệu riêng tư).

---

<div align="center">

**Developed by [Việt Trần](https://github.com/viettd14)**  
**Smart PiP · v2.0.0 Stable**

⭐ Nếu dự án hữu ích, bạn có thể Star repository để theo dõi các bản cập nhật.

</div>
