**🇻🇳 Tiếng Việt** · [🇬🇧 English](README.en.md)

# TradingAutoTV — đọc tín hiệu trên chart TradingView, vào lệnh MT5 / Binance Futures

**TradingAutoTV** là app trên Windows đọc **thẳng biểu đồ TradingView** bạn đang mở (lệnh của strategy, biểu tượng, nhãn chữ của chỉ báo…) rồi vào lệnh trên **MetaTrader 5** hoặc **Binance USDⓈ-M Futures** theo luật bạn đặt. Không cần tạo alert, không cần webhook.

### 👉 [Tải bản mới nhất](https://github.com/xahoapro/tradingautotv-releases/releases/latest) · [Giới thiệu tool](https://tradingauto.org/toolintroduce/tradingview) · [Đăng ký tài khoản](https://tradingauto.org/register) · [Mua key](https://tradingauto.org/Pricing#tvbot)

---

## ✨ Tính năng

**📈 Đọc tín hiệu ngay trên chart**
- Gắn với TradingView Desktop (hoặc Chrome / Edge) đang mở, đọc layout, biểu đồ và chỉ báo — chỉ đọc, không sửa chart của bạn.
- Đối tượng kích hoạt: lệnh của strategy, biểu tượng, nhãn chữ, vạch, vùng… App đề xuất sẵn theo tên (Long → mở BUY, Short Exit → đóng SELL).
- Điều kiện BẤT KỲ / TẤT CẢ / ÍT NHẤT k trong một số nến, kèm bộ lọc theo chỉ báo khác.

**🤖 Trình tạo bot 5 bước**
- Nguồn → Điều kiện → Quy ước vào lệnh → Vốn → Xem lại.
- SL / TP đặt sẵn hoặc lấy theo đối tượng trên chart; nhiều mức TP chốt theo %; trailing; hoà vốn sau TP1; bỏ lệnh khi giá chạy xa.
- Lô cố định hoặc theo rủi ro (USD / % equity), trần lô, ngừng khi lỗ / lãi đủ % equity.
- **Magic và comment riêng cho từng bot** để lọc, phân loại lệnh trên MT5.

**🛡️ An toàn trước đã**
- Bot mới luôn ở **CHỈ THEO DÕI**: đọc chart, MT5 kiểm lệnh nhưng không gửi — xem nhật ký đúng rồi mới chuyển **VÀO LỆNH**.
- Layout bị đổi, chart thu nhỏ, tài khoản rớt mạng… bot **tạm dừng mở lệnh mới** nhưng vẫn đóng / sửa lệnh cũ; đúng lại là tự chạy tiếp.
- Tài khoản THẬT phải gõ lại số tài khoản để xác nhận; thanh trên chuyển đỏ khi có bot vào lệnh thật.
- Bot đang chạy lúc tắt app thì mở lại app tự chạy lại (tắt được từng bot).

**🏦 Nhiều tài khoản**
- Mỗi tài khoản MT5 một terminal **sạch** do app nhân bản (không EA của ai, không mật khẩu đã lưu), chạy ẩn, có EA thừa hành để đóng lệnh hàng loạt nhanh.
- Sàn chưa có trên máy: app hiện MT5 cho bạn đăng nhập tay **một lần**, lần sau tự dùng lại.
- **Binance USDⓈ-M Futures** (mới): testnet hoặc thật, SL / TP đặt ngay trên sàn. App từ chối API key có quyền rút tiền.
- Mật khẩu / API key chỉ đi qua 127.0.0.1 và được mã hoá bằng Windows (DPAPI).

**📋 Nhật ký & tổng quan**
- Một màn tổng quan cho mọi bot, tài khoản và việc cần xử lý; nhật ký đầy đủ từng tín hiệu, từng lệnh.
- Giao diện Tiếng Việt / English; trang **Sản phẩm khác** giới thiệu các tool TradingAuto khác.

## 🔑 License key

- Vào lệnh cần **license key TradingView Bot của TradingAuto**. Một key cấp cho một tài khoản và chạy ở một nơi (app này, EA hoặc MT5 Manager).
- **Mua key:** mở [Bảng giá](https://tradingauto.org/Pricing#tvbot) → chọn mục **📡 TradingView Bot** → mua theo hướng dẫn trên web (cần tài khoản tradingauto.org — chưa có thì [đăng ký](https://tradingauto.org/register) trước). Nút **Mua key** trong app mở đúng trang này.
- **Tài khoản demo** và tài khoản mở dưới **IB TradingAuto** dùng key thành viên `vipmember` có sẵn trong app — **miễn phí**.
- Không có key vẫn thêm tài khoản, tạo bot và chạy CHỈ THEO DÕI được — chỉ không gửi lệnh mới.

## 🚀 Bắt đầu

1. **[Tải bộ cài](https://github.com/xahoapro/tradingautotv-releases/releases/latest)**: file `TradingAutoTV-<phiên bản>-setup.exe`, chạy để cài (không cần quyền admin; mặc định vào `%LOCALAPPDATA%\Programs\TradingAutoTV`, có lối tắt ở Start Menu). Windows hiện "Windows protected your PC" thì bấm **More info → Run anyway**.
2. Mở TradingView Desktop kèm tham số `--remote-debugging-port=9222` (hoặc Chrome / Edge hồ sơ riêng, cổng 9223) và đăng nhập TradingView.
3. Trong app: **License key** → **Tài khoản MT5** (hoặc Binance) → **＋ Bot từ layout này** → chạy CHỈ THEO DÕI → xem nhật ký → **Chuyển VÀO LỆNH**.

Mục **Hướng dẫn** trong app có từng bước chi tiết.

## 💻 Yêu cầu

- Windows 10 / 11 64-bit.
- Đã cài MetaTrader 5 (app nhân bản terminal từ bản cài của bạn) — hoặc tài khoản Binance Futures.
- TradingView Desktop hoặc Chrome / Edge. Mỗi layout bot dùng nên ở một cửa sổ riêng, không thu nhỏ (TradingView ngừng cập nhật chart bị thu nhỏ).
- Máy phải bật và có mạng thì bot mới chạy (dùng VPS Windows để chạy 24/7).

## 🔄 Cập nhật

App tự báo khi có bản mới, bấm là tải và cài; bản mới hỏng thì tự quay lại bản cũ, dữ liệu (`data\`) giữ nguyên. Gói cập nhật được **ký số** — app chỉ nhận bản chính thức.
File `-update.zip` và `latest.json` trong mục Releases dành cho cơ chế tự cập nhật — khách mới hãy tải file **`-setup.exe`**.

## 💬 Hỗ trợ & cộng đồng

- Website: **[tradingauto.org](https://tradingauto.org)**
- Nhóm Zalo: [zalo.me/g/scuqhg283](https://zalo.me/g/scuqhg283) · Nhóm Telegram: [t.me/autotradingfreeall](https://t.me/autotradingfreeall)
- Các tool khác: [MT5 Manager](https://github.com/xahoapro/mt5manager-releases) · [Copytrade Online](https://tradingauto.org/toolintroduce/copytrade) · [Smart DCA](https://tradingauto.org/toolintroduce/dcabot) · [Copy Signal → MT5](https://tradingauto.org/toolintroduce/signaltrader)

> ⚠️ TradingAutoTV thực hiện đúng luật bạn đặt — **không dự đoán thị trường và không bảo đảm lợi nhuận**. Giao dịch ngoại hối / CFD / hợp đồng tương lai tiền mã hoá có rủi ro cao. Hãy chạy CHỈ THEO DÕI và tài khoản demo trước.
