# 坡度計算機 · Slope Calculator

輸入**長度**與**前後高差**，即時換算**坡度（%）、斜率（1:n）、‰、角度（°）**，並附上剖面圖與台灣常用法規提醒。工地、設計、滑雪都適用。

🔗 **線上使用**：https://radihuang.github.io/slope-calculator/

## 功能

- **正算**：長度（可切「水平長度／斜距」）＋ 前後高差 → 坡度、斜率、‰、角度。
- **反算**：給定目標坡度（`1:n` 或 `%`）＋ 已知一邊，反推所需高差或水平長。
- **常用情境一鍵套用**：浴室洩水、淋浴濕區、屋頂洩水、無障礙坡道、車道。
- **法規提醒**（以水平投影長計）：
  - 洩水坡度 — 小洩 1/100、大洩 1/50（下限判定）
  - 車道坡道 — 上限 1:6（建築技術規則建築設計施工編 §61）
  - 無障礙坡道 — 上限 1/12，含高差 < 20cm 放寬表（建築物無障礙設施設計規範 206）
  - 滑雪難度概略分級（綠／藍／黑／雙黑）
- **剖面圖**：依實際坡度傾斜的小圖示，可選 滑單板／車輛／輪椅。
- **複製結果**：輸出成一行文字，方便貼進施工筆記。

## 本地開啟

純靜態單檔，直接用瀏覽器打開即可：

```bash
open index.html          # macOS
# 或用本地伺服器（擇一）
python3 -m http.server   # 開 http://localhost:8000
```

## 部署（GitHub Pages）

1. 推上 `main` 分支。
2. Repo → **Settings → Pages** → Source 選 `Deploy from a branch`，Branch 選 `main` / `root`。
3. 稍候即可於 `https://radihuang.github.io/slope-calculator/` 使用。

技術上採 React 18 + Babel standalone（CDN 載入、瀏覽器端即時編譯），不需 `npm install` 或 build。

## 檔案結構

```
slope-calculator/
├── index.html   # 主程式（自包含）
├── README.md
├── LICENSE      # MIT
├── .gitignore
└── icons/       # 圖示原始 SVG（可編輯原檔）
    ├── slope_car.svg
    ├── slope_wheelchair.svg
    └── slope_snowboarder.svg
```

## 免責聲明

法規數值為現行常見規定之整理，僅供快速研判參考。實際設計與查驗請以**最新條文與主管機關認定**為準。滑雪難度分級為國際慣例概略值，各雪場略有差異。

## 授權

[MIT](LICENSE) © radihuang　圖示為作者自繪。
