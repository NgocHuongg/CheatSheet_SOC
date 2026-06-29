# CheatSheet_SOC

Bộ cheat sheet phục vụ công việc **SOC / Threat Hunting / DFIR** — ánh xạ các sự kiện log Windows sang hành vi tấn công kèm kỹ thuật **MITRE ATT&CK**.

Mỗi cheat sheet là một file HTML độc lập (mở trực tiếp bằng trình duyệt, không cần cài đặt), có sẵn tìm kiếm, lọc theo nhóm hành vi, dark mode và responsive.

## Nội dung

| Cheat sheet | Mô tả |
|---|---|
| [`SysmonID_mapping_Malware.html`](SysmonID_mapping_Malware.html) | Ánh xạ **Sysmon Event ID** (1–29) sang hành vi malware: process injection, persistence, C2, evasion… |
| [`WindowsEventID_mapping_Attack.html`](WindowsEventID_mapping_Attack.html) | Ánh xạ **Windows Event ID** native (Security / System / PowerShell / WMI / AppLocker…) sang hành vi tấn công: brute force, Kerberoasting, Pass-the-Hash, lateral movement, log clearing… |

## Cách dùng

1. Tải hoặc clone repo:
   ```bash
   git clone https://github.com/NgocHuongg/CheatSheet_SOC.git
   ```
2. Mở file `.html` bất kỳ bằng trình duyệt.
3. Dùng ô tìm kiếm để lọc theo Event ID, tên event, kỹ thuật MITRE; hoặc bấm chip để lọc theo nhóm hành vi.
4. Bấm vào một dòng để xem chi tiết các hành vi tấn công tương ứng.

## Ghi chú

- Phục vụ mục đích **phòng thủ / phát hiện** (defensive security, detection engineering).
- Tham chiếu MITRE ATT&CK technique ID để dễ tra cứu chéo và xây dựng detection rule.
