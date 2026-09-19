# Mint

![Latest release](https://img.shields.io/github/v/release/makenode-vn/mint-releases?label=phi%C3%AAn%20b%E1%BA%A3n%20hi%E1%BB%87n%20t%E1%BA%A1i)
![Platforms](https://img.shields.io/badge/platform-Windows%20%7C%20macOS-blue)

**Mint** là ứng dụng báo giá gia công kỹ thuật số — thả file 3D (STL, OBJ, 3MF) vào, nhận báo
giá ngay lập tức. Phát triển bởi **MakeNode**.

*(Mint is a digital manufacturing quoting app — drop a 3D file, get an instant price.
Developed by MakeNode.)*

## Tải về (Download)

Vào tab **[Releases](https://github.com/makenode-vn/mint-releases/releases)** của repo này,
chọn bản mới nhất, tải file phù hợp với máy bạn:

| Hệ điều hành | File cần tải |
|---|---|
| Windows | `.exe` (NSIS installer) |
| macOS (Apple Silicon / M1 trở lên) | `.dmg` |

> macOS hiện chưa có chữ ký Apple Developer ID, nên lần mở đầu tiên có thể bị Gatekeeper cảnh
> báo "unidentified developer" — chuột phải vào app → **Open** để mở bình thường.

## Cập nhật tự động (Auto-update)

Mint tự kiểm tra bản mới mỗi khi mở app, và định kỳ sau đó — **nhưng không tự tải hay cài đặt
gì nếu bạn chưa đồng ý**. Khi có bản mới, app sẽ hỏi bạn có muốn cập nhật không; nếu đồng ý,
app tải về rồi hỏi lại lần nữa trước khi khởi động lại để áp dụng. Bạn luôn có thể chọn "Để
sau" ở cả hai bước.

Có thể kiểm tra cập nhật thủ công bất cứ lúc nào: mở Mint → menu **Help** → tab **About** →
**Check for Updates**.

Người dùng thử nghiệm nội bộ có thể bật kênh **Beta** ở Settings → Update Channel để nhận bản
thử nghiệm sớm hơn (có thể kém ổn định hơn bản chính thức).

---

*Repo này chỉ chứa file cài đặt, không chứa mã nguồn — mã nguồn của Mint nằm ở một repo riêng
tư khác. Dành cho developer: xem
[ADR-007](https://github.com/makenode-vn/monorepo/blob/main/mint/docs/decisions/adr-007-ci-cd.md#update-2026-09-19-auto-update-windows--macos)
và [`releasing.md`](https://github.com/makenode-vn/monorepo/blob/main/mint/docs/releasing.md)
để biết vì sao repo này tồn tại và cách phát hành bản mới.*
