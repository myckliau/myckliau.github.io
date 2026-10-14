# 🔌 GPIO 控制與圖片生成面板 (GPIO Controller & Image Generator)

這是一個整合 **ESP32** 與 **Raspberry Pi (樹莓派)** 的 GPIO 腳位規劃與視覺化中心。本專案透過網頁介面提供直觀的 GPIO 腳位配置、線上編輯功能，並能根據設定動態更新對應的硬體腳位圖片。

## 🌐 專案首頁預覽
透過根目錄的 `index.html`，您可以一鍵切換至不同的硬體控制端點：
* **ESP32 GPIO 面板** (`/esp32_gpio/index.htm`)
* **Raspberry Pi GPIO 面板** (`/rasperberry_gpio/index.htm`)

---

## 📂 專案目錄結構
```text
├── index.html             # 專案入口首頁（控制台）
├── README.md              # 本說明文件
├── esp32_gpio/
│   └── index.htm          # ESP32 GPIO 規劃與圖片生成網頁
└── rasperberry_gpio/
    └── index.htm          # Raspberry Pi GPIO 規劃與圖片生成網頁
```

---

## ✨ 核心功能
* **🚀 雙平台整合規劃**：一鍵切換 ESP32 與 Raspberry Pi 的微控制器專屬規劃網頁。
* **✏️ 線上互動編輯**：
  * **自訂功能說明**：可針對每個 GPIO 腳位手動輸入或修改自訂的功能備註。
  * **切換 In/Out 模式**：自由設定腳位為輸入（Input）或輸出（Output）狀態。
  * **更換接點顏色**：支援自訂各個接點顏色，方便依功能（如電源、通訊、訊號）進行視覺化分類。
* **🖼️ 圖片自適應生成**：根據目前編輯的功能說明、In/Out 狀態與接點顏色，網頁會即時更新並呈現相對應的自訂硬體腳位圖。
* **💾 JSON 配置備份與還原**：
  * **匯出 JSON**：一鍵將當前所有腳位的功能說明、In/Out 狀態與接點顏色打包下載為 `.json` 檔案。
  * **載入 JSON**：支援將先前保存的 `.json` 檔案重新匯入網頁，即可**即時復原所有的腳位設定並自動生成完全相同的對應圖片**，方便分享、存檔與跨設備同步。

---

## 🛠️ 使用與部署說明

### 1. 本地端使用 (Local)
直接將此專案下載（或 `git clone`）到電腦中，雙擊打開根目錄的 `index.html` 即可透過瀏覽器開始使用。

### 2. GitHub Pages 靜態網頁託管
本專案完全由 HTML/CSS/JavaScript 組成，非常適合直接使用 **GitHub Pages** 進行免費線上部署：
1. 將專案推送到 GitHub 儲存庫。
2. 進入儲存庫的 **Settings** > **Pages**。
3. 在 *Build and deployment* 的 Build 來源選擇 `Deploy from a branch`。
4. 將 Branch 設為 `main` (或你的預設分支) / `/(root)`，並點擊 **Save**。
5. 稍等 1-2 分鐘後，即可透過 GitHub 提供的專屬網址線上存取您的控制面板！

---

## 📝 備註
* 子資料夾內的網頁檔案格式為 `.htm`，主控制台已做好相對路徑對接，請勿隨意更動資料夾名稱，以免連結失效。
