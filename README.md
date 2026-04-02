# 🎈 demo-first-streamlit

[![Streamlit](https://img.shields.io/badge/Streamlit-1.x-FF4B4B.svg)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Google Sheets](https://img.shields.io/badge/Google%20Sheets-API-34A853.svg)](https://developers.google.com/sheets)

## 🌐 Live Demo

| App | 說明 | 連結 |
|-----|------|------|
| 🎈 **demo.py** | 基礎 Streamlit 元件展示 | [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://demo-first-app-jy5qjx235vxuzwx8qetzsm.streamlit.app/) |
| 📊 **crud-app.py** | Google Sheets CRUD 儀表板 | [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://demo-first-app-iddmloyzq6ukwivrydv8pn.streamlit.app/) |

---

## 📋 專案概述

Streamlit 學習歷程，從基礎互動元件展示，到整合 Google Sheets API 的完整 CRUD 儀表板。用純 Python 打造互動式 Web App，無需撰寫任何 HTML / CSS / JavaScript。

---

## 📁 檔案說明

| 檔案 | 說明 |
|------|------|
| `demo.py` | 基礎 Streamlit 元件：文字輸入、互動回應、折線圖、側邊欄 |
| `crud-app.py` | Google Sheets CRUD：讀取、新增、修改、刪除資料 |
| `requirements.txt` | 套件需求清單 |

---

## ✨ 功能說明

### 🎈 demo.py — 基礎元件展示

- `st.title` / `st.write` / `st.success` 基礎文字元件
- `st.text_input` 互動輸入，即時顯示歡迎訊息
- `pandas` + `numpy` 隨機數據，`st.line_chart` 折線圖
- `st.sidebar` 側邊欄設定區塊

### 📊 crud-app.py — Google Sheets CRUD 儀表板

- **Read** — 讀取 Google Sheets 所有資料並以 DataFrame 顯示
- **Create** — 表單新增資料，即時寫入 Google Sheets
- **Update** — 選擇列號，修改姓名與數量欄位
- **Delete** — 選擇列號，確認後刪除並自動刷新頁面

---

## 🛠️ 技術棧

| 技術 | 說明 |
|------|------|
| **Streamlit** | 純 Python 打造互動式 Web App |
| **gspread** | Google Sheets Python API |
| **pandas** | 資料處理與 DataFrame 顯示 |
| **numpy** | 隨機數據生成 |
| **Streamlit Cloud** | 免費部署，自動從 GitHub 同步 |

---

## 🚀 本地執行

```bash
# 1. 安裝套件
pip install -r requirements.txt

# 2. 執行基礎展示 App
streamlit run demo.py

# 3. 執行 CRUD App（需先設定 Google Sheets 憑證）
streamlit run crud-app.py
```

---

## 🔑 Google Sheets 憑證設定（crud-app.py）

### 本機開發

在專案根目錄建立 `.streamlit/secrets.toml`：

```toml
[gcp_service_account]
type = "service_account"
project_id = "your-project-id"
private_key_id = "your-key-id"
private_key = "-----BEGIN RSA PRIVATE KEY-----\n...\n-----END RSA PRIVATE KEY-----\n"
client_email = "your-service-account@project.iam.gserviceaccount.com"
client_id = "your-client-id"
```

### Streamlit Cloud 部署

1. 前往 Streamlit Cloud → App 設定 → **Secrets**
2. 貼上上方 `secrets.toml` 內容
3. 將服務帳號 email 加入 Google Sheets 的共用編輯者

---

## ☁️ Streamlit Cloud 部署步驟

1. Push 程式碼到 GitHub
2. 前往 [share.streamlit.io](https://share.streamlit.io/)
3. 選擇 repo 與要執行的 Python 檔案
4. 設定 Secrets（crud-app.py 需要）
5. 點擊 Deploy

---

*劉玳如 Tai-Ju Liu*
