# WindVoice Master Spec — CLEAN v6.0

版本：v6.0 CLEAN  
建立日期：2026-07-01  
主要整理 AI：ChatGPT / Nick  
狀態：主規格 SSOT  
位置：docs/00_MASTER.md  

---

## 1. 本文件用途

這份文件是 WindVoice 的主規格文件。

它是目前專案的 SSOT，也就是 Single Source of Truth。

後續所有 AI、開發工具、工程師、測試版本，都應該優先依照本文件執行。

---

## 2. 產品定位

WindVoice 是一個聲音分析工具。

核心目標：

**WindVoice 讓你看見你自己的聲音。**

WindVoice 不是唱歌評分軟體。  
WindVoice 不是 KTV 娛樂軟體。  
WindVoice 不是醫療診斷工具。  
WindVoice 不是主觀歌唱老師。

---

## 3. 核心原則

1. 只分析可測量的聲學資料。
2. 不使用主觀評分。
3. 不說「唱得好」或「唱得不好」。
4. 不使用醫療診斷語言。
5. 低信心資料不下結論。
6. 每個分析結果都應附限制與信心。
7. 以清唱或乾淨人聲輸入為優先。
8. 文字說明要正向、精準、可理解。

---

## 4. 主要分析項目

WindVoice 主要分析：

- Pitch 音高
- Cent Deviation 音準偏差
- Range 音域
- Comfortable Range 舒適音區
- Resonance 共鳴
- Harmonics 泛音
- Vibrato 顫音
- Stability 穩定度
- Energy Distribution 能量分布
- Confidence 分析信心

---

## 5. 輸入資料規則

允許：

- 清唱錄音
- 純伴奏搭配人聲
- 上傳音訊檔
- 上傳影片檔中的音訊

不建議：

- 原唱混入
- 半消音導唱
- 大量混響
- 嚴重環境噪音
- 人聲殘留過多的伴奏

---

## 6. UI 視覺方向

整體風格：

- 黑
- 白
- 金
- 簡潔
- 留白
- 避免炫彩
- 避免過度科技感

主要視覺規則：

- 主音：白色
- 泛音：金色
- 頻譜主視圖：0–2000Hz
- 圖表可展開查看細節
- 手機版優先清楚易用

---

## 7. 基本使用流程

1. 使用者開啟 WindVoice。
2. 使用者選擇錄音或上傳音檔。
3. 使用者填寫基本前置資訊。
4. 系統檢查輸入品質。
5. 系統分析聲音資料。
6. 系統產生圖表與文字說明。
7. 使用者儲存或比較歷史紀錄。

---

## 8. 專案結構

```text
WindVoice
│
├── README.md
│
├── docs/
│   ├── 00_MASTER.md
│   ├── 01_OVERVIEW.md
│   ├── 02_REQUIREMENTS.md
│   ├── 02_AI_RULES.md
│   ├── 03_TECH/
│   ├── 04_UI/
│   ├── 05_AUDIO_ENGINE/
│   ├── 06_TESTING/
│   └── 07_DISCUSSION_INSIGHTS/
│
├── src/
│   ├── audio/
│   ├── analysis/
│   ├── ui/
│   ├── data/
│   └── utils/
│
└── archive/
    └── old_files/
