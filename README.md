# ccremote-release

Kênh phát hành công khai của **ccremote** (*code chat remote*): điều khiển coding agent đang chạy trên máy
tính của bạn từ điện thoại, như một app chat. Mã nguồn nằm ở repo riêng; repo này chỉ chứa bản build
(GitHub Releases) và manifest mà app đọc để tự cập nhật.

## Cài đặt

- **Android**: tải `ccremote-<version>.apk` ở Release `android-v…` mới nhất. Lần đầu Android hỏi quyền cài
  ứng dụng từ nguồn này.
- **Windows**: tải `ccremote_<version>_x64-setup.exe` ở Release `desktop-v…` mới nhất.

Cài một lần, sau đó app tự báo và cài bản mới.

## Manifest tự cập nhật

| File | Dùng bởi |
|---|---|
| `android/latest.json` | App Android: `version_code`, `apk_url`, `sha256` của APK |
| `desktop/latest.json` | App desktop (Tauri updater): bộ cài kèm chữ ký minisign |

Không sửa tay các file này — script phát hành ghi chúng sau khi đăng bản build.
