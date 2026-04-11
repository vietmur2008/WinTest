# 🪟 WinTest — Windows 12 Testing Suite

> A comprehensive testing toolkit for Windows 12 — covering UI/UX, Performance Benchmarks, and Software Compatibility.

![License](https://img.shields.io/badge/license-MIT-blue)
![Platform](https://img.shields.io/badge/platform-Windows%2012-blueviolet)
![Languages](https://img.shields.io/badge/languages-Python%20%7C%20C%2B%2B%20%7C%20C%23%20%7C%20PowerShell-orange)
![Status](https://img.shields.io/badge/status-active-brightgreen)

---

## 📦 Project Structure

```
WinTest/
├── README.md
├── .github/
│   └── workflows/
│       └── ci.yml
├── ui-ux/                      # Python — UI/UX automation & screenshot tests
│   ├── requirements.txt
│   └── tests/
│       ├── test_taskbar.py
│       ├── test_start_menu.py
│       └── test_settings.py
├── benchmark/                  # C++ — CPU, RAM, Disk performance benchmarks
│   ├── CMakeLists.txt
│   └── src/
│       ├── main.cpp
│       ├── cpu_bench.cpp
│       ├── ram_bench.cpp
│       └── disk_bench.cpp
├── compatibility/              # C# .NET — Software compatibility checker
│   ├── WinTest.Compatibility.csproj
│   └── src/
│       ├── Program.cs
│       ├── AppScanner.cs
│       └── DriverChecker.cs
└── scripts/                    # PowerShell — System info & automation
    ├── system_info.ps1
    ├── run_all_tests.ps1
    └── generate_report.ps1
```

---

## 🧪 Modules

### 1. 🖥️ UI/UX Testing (`ui-ux/`) — Python
Tests the visual and interactive aspects of Windows 12.
- Taskbar layout and behavior
- Start Menu responsiveness
- Settings panel navigation
- Screenshot diffing against baselines

**Dependencies:** `pyautogui`, `pillow`, `pytest`

```bash
cd ui-ux
pip install -r requirements.txt
pytest tests/
```

---

### 2. ⚡ Benchmark (`benchmark/`) — C++
Measures raw system performance on Windows 12.
- CPU single/multi-core throughput
- RAM read/write speed
- Disk sequential & random I/O

**Build:**
```bash
cd benchmark
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
./build/WinBench
```

---

### 3. 🔗 Compatibility (`compatibility/`) — C# .NET
Scans installed applications and drivers for Windows 12 compatibility.
- Detects legacy 32-bit apps
- Flags unsigned or outdated drivers
- Generates a compatibility report (JSON + HTML)

**Run:**
```bash
cd compatibility
dotnet run
```

---

### 4. 🛠️ Scripts (`scripts/`) — PowerShell
Utility scripts for automation and reporting.
- Collect full system specs
- Run all test modules in sequence
- Export unified HTML report

**Run:**
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
.\scripts\run_all_tests.ps1
```

---

## 🚀 Quick Start

```powershell
# Clone the repo
git clone https://github.com/yourusername/WinTest.git
cd WinTest

# Run everything
.\scripts\run_all_tests.ps1
```

---

## 📊 Sample Report Output

| Module         | Status    | Score / Result          |
|----------------|-----------|-------------------------|
| UI/UX Tests    | ✅ Pass   | 42/42 tests passed      |
| CPU Benchmark  | ✅ Done   | 18,450 pts (multi-core) |
| RAM Benchmark  | ✅ Done   | 48.2 GB/s read speed    |
| Disk Benchmark | ✅ Done   | 3,200 MB/s sequential   |
| Compatibility  | ⚠️ Warn   | 3 legacy apps flagged   |

---

## 🤝 Contributing

Pull requests are welcome! Please open an issue first to discuss what you'd like to change.

---

## 📄 License

[MIT](LICENSE) © 2026 WinTest Contributors

