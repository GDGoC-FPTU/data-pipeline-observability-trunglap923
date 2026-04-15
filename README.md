[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574012&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** trunglap923@gmail.com
**Name:** Vũ Trung Lập

---

## Mo ta

Bai lab nay xay dung mot ETL pipeline đe xu ly du lieu san pham:
- **Extract:** Đoc du lieu tu `raw_data.json`
- **Validate:** Loai bo du lieu khong hop le (gia am, category trong)
- **Transform:** Them discount, normalize category, timestamp
- **Load:** Luu ket quq vao `processed_data.csv`
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

**ETL Pipeline Results:**
- Tong so records dau vao: 5 records tu raw_data.json
- Records hop le: 3 records duoc luu vao processed_data.csv
- Records bi loai bo: 2 records (1 co gia am, 1 co category trong)

**Stress Test Results:**
- Clean Data: Agent tim dung san pham tot nhat (Laptop)
- Garbage Data: Agent sai do du lieu kem chat luong (Nuclear Reactor)

**Transformation Details:**
- Da them discount cho moi san pham
- Normalize category thanh chu thường
- Them timestamp cho moi record

