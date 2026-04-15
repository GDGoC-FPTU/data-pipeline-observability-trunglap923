# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600347
**Name:** Vũ Trung Lập
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | 10 | Agent tra ve ket qua chinh xac la Laptop voi gia $1200. |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 1 | Agent tra ve Nuclear Reactor vi gia cao nhat va danh muc sai lech. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Agent tra loi sai khi dung Garbage Data vi du lieu dau vao chua nhieu loi nghiem trong ma Agent khong the tu nhan biet. Thu nhat, co loi Duplicate IDs (ID 1 xuat hien 2 lan cho Laptop va Banana), gay nhiu loan dinh danh. Thu hai la Wrong Data Types, cot gia cua "Broken Chair" la chuoi van ban "ten dollars" thay vi so, co the gay loi tinh toan. Thu ba, quan trong nhat la su xuat hien cua Outliers hoac du lieu sai lech hoan toan nhu "Nuclear Reactor" voi gia cuc cao ($999999) duoc gan vao danh muc 'electronics'. Do thuat toan cua Agent chi don gian la tim san pham co gia cao nhat trong danh muc yeu cau, no da tin tuong va de xuat san pham vo ly nay. Ngoai ra con co cac gia tri trong (Null values) o dong cuoi cung. Tat ca nhung dieu nay chung minh rang Agent chi thong minh dua tren du lieu no nhan duoc; du lieu rac se dan den ket qua rac.

---

## 3. Ket luan

Toi hoan toan dong y rang Quality Data > Quality Prompt. Du prompt co duoc toi uu hoa den dau ("Hay tim san pham dien tu tot nhat"), neu du lieu co so chua thong tin sai lech nhu "Lo phan ung hat nhan" la do dien tu, Agent van se dua ra ket qua sai. "Garbage in, Garbage out" la nguyen tac bat di bat dich trong AI va RAG.
