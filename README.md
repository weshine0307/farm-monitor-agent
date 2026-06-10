# 農場環境監測「異常提醒」AI Agent

一個**可互動的生成式 AI 應用情境原型**：把農場 IoT 感測器產生的環境時序資料，從「要人盯的數字」變成「會主動開口、看得懂、給得出建議」的 AI Agent。

> ⚠️ 本頁為**應用情境規劃原型**：研判文字以規則生成（情境模擬），非即時呼叫 LLM。頁面同時攤開設計中的 RAG → Prompt → 生成 pipeline，展示應用架構而非假裝 live。

## 核心功能

- **AI Agent 研判**：持續比對 RAG 知識庫中各作物的環境適宜區間與風險閾值，自動偵測寒害／缺水／積水等異常
- **主動推播**：偵測異常 → 生成白話處置建議 → 推播（示意 LINE OA）→ 處置紀錄回存知識庫
- **空間定位**：將異常風險定位至特定地塊（Leaflet 地圖），輔助判斷處置優先順序
- **透明化 pipeline**：每筆研判可展開「RAG 檢索 → 組裝 Prompt → 模型生成」三步，展示生成式 AI 應用的服務流程與資料架構設計

## 技術

- 純前端：HTML / CSS / Vanilla JS
- 地圖：Leaflet + GeoJSON（底圖 © OpenStreetMap、CARTO）
- 字型：jf-openhuninn 2.1（自帶於 `fonts/`）

## 結構

```
farm-monitor-agent/
├── index.html                 # 主頁（自給自足，雙擊即可開）
├── fonts/jf-openhuninn-2.1.ttf
└── images/farm_monitor_cover.jpg
```

## 部署

線上版透過 portfolio repo 部署於 **wschtw.com/farm-monitor/**。
本 repo 為專案來源；portfolio 內 `farm-monitor/` 為部署副本，內容修改需兩邊同步。

---

規劃／製作：陳薇珊 Wei-Shan Chen · GIS × 生成式 AI
