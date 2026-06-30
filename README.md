# CheatSheet_SOC

Bộ cheat sheet tổng hợp để dùng trong công việc **SOC / Threat Hunting / DFIR** — ánh xạ log Windows và các kỹ thuật tấn công sang **MITRE ATT&CK** cho dễ tra cứu khi điều tra.

Mỗi file là một trang HTML độc lập, mở thẳng bằng trình duyệt để dễ dàng tương tác với từng mục. 

## Nội dung

| Cheat sheet | Mô tả |
|---|---|
| [`SysmonID_mapping_Malware.html`](SysmonID_mapping_Malware.html) | Ánh xạ **Sysmon Event ID** (1–29) sang hành vi malware: process injection, persistence, C2, evasion… |
| [`WindowsEventID_mapping_Attack.html`](WindowsEventID_mapping_Attack.html) | Ánh xạ **Windows Event ID** native (Security / System / PowerShell / WMI / AppLocker…) sang hành vi tấn công: brute force, Kerberoasting, Pass-the-Hash, lateral movement, log clearing… |
| [`WindowsAPI_mapping_Malware.html`](WindowsAPI_mapping_Malware.html) | Ánh xạ **Windows API** sang hành vi malware: process hollowing, shellcode injection, hook, APC queue, token impersonation… |
| [`LOLBAS_mapping_Sysmon.html`](LOLBAS_mapping_Sysmon.html) | **Living Off The Land Binaries** — 34 LOLBin phổ biến (mshta, rundll32, certutil, wmic, cmstp…) với command line điển hình để download / execute / persistence, kèm pattern phát hiện theo **Sysmon EID 1** và kỹ thuật MITRE. |

## Cách dùng

1. Clone repo:
   ```bash
   git clone https://github.com/NgocHuongg/CheatSheet_SOC.git
   ```
2. Mở file `.html` bằng trình duyệt.
3. Dùng ô tìm kiếm để lọc theo tên event / binary / kỹ thuật MITRE / command line.
4. Bấm vào một dòng để xem chi tiết hành vi và detection note.

## Ghi chú

- Mục đích **phòng thủ / phát hiện** (detection engineering, threat hunting), không dùng cho mục đích tấn công.
- Tham chiếu MITRE ATT&CK technique ID để tra cứu chéo và viết detection rule.
- Nguồn tham khảo LOLBAS: [lolbas-project.github.io](https://lolbas-project.github.io/)
