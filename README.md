# Life Quest 🏰

> **將生活遊戲化，用行動堆砌你的高塔。**
> *Gamify your life, build your legacy.*
結合了 RPG 遊戲化元素、番茄鐘專注工具以及情緒管理功能，旨在幫助使用者通過完成日常任務來獲得視覺上的成就感。
> https://progress01.github.io/lifecheck/

## ✨ 特色功能 (Features)

### 1. ⚔️ 任務系統 (Quest Board)

採用三欄式看板設計，針對不同類型的任務給予不同回饋：

* **習慣 (Habits) `黃色**`：可無限點擊，累積經驗值（Legacy），適合培養微習慣（如喝水）。
* **每日 (Daily) `藍色**`：每日重置狀態，適合規律的日常作息。
* **待辦 (Quest) `橘色**`：一次性任務，完成後封存並計入生涯累積。

### 2. 🏗️ 視覺化成就 (Visual Legacy)

* **動態高塔**：背景 Canvas 會根據你的「生涯累積數值 (Legacy)」自動繪製一座不斷增高的高塔。
* **粒子特效**：完成任務或清除項目時，會有粒子爆炸的視覺回饋。
* **日夜循環**：背景天空顏色會根據現實時間（早/晚）自動切換。
* **成就徽章**：當累積數值達到特定里程碑 (10, 50, 100, 500) 時解鎖像素風徽章。

### 3. 🔮 實用工具箱 (Utility Kit)

* **命運指引 (Gacha)**：猶豫不決時，從「挑戰池」中隨機抽取一個任務。
* **情緒碎紙機 (Void)**：寫下焦慮或負面念頭，按下按鈕將其「粉碎」（視覺與音效回饋）。
* **專注結界 (Focus)**：內建 25 分鐘番茄鐘倒數，搭配全螢幕遮罩，強制進入專注狀態。
* **每日日誌 (Journal)**：快速記錄心情（Emoji）與簡短心得。

### 4. 💾 輕量化技術 (Tech Specs)

* **Single File Component**：所有 HTML, CSS, JS 都在一個檔案中，無需伺服器，雙擊即開。
* **Offline First**：使用瀏覽器 `localStorage` 儲存資料，隱私且無需網路。
* **Responsive**：適配手機版面 (Mobile-first)，支援 PWA 風格的底部導航欄。
* **8-bit Sound**：內建 Web Audio API 生成的復古音效。

## 🚀 如何使用 (Usage)

1. **啟動**：直接用瀏覽器（Chrome/Safari/Edge）打開 `index.html`。
2. **新增任務**：點擊右下角的 `+` 懸浮按鈕 (FAB)。
3. **互動**：
* 點擊方框完成任務。
* 點擊頂部天空區域可切換視角（查看高塔頂端）。
* 點擊「冒險指引」卡片可編輯你的座右銘。


4. **備份**：前往「設定」頁面點擊「備份資料」，可匯出 JSON 檔。

## 🛠️ 自定義與開發 (Customization)

若您是開發者，可直接編輯原始碼中的 `:root` 變數與 `const app` 邏輯：

* **配色修改**：在 `<style>` 的 `:root` 區域修改 `--primary`, `--habit` 等變數。
* **遊戲平衡**：在 script 中的 `const badges` 修改成就解鎖門檻。
* **音效調整**：在 `const sfx` 物件中調整頻率與波形。

## 📂 檔案結構

```text
index.html
├── <style>       # CSS (包含 Glassmorphism UI 與動畫)
├── <canvas>      # 背景繪圖層 (Particle system & Tower generation)
├── <html>        # DOM 結構 (Tab頁面切換機制)
└── <script>      # 核心邏輯 (Vanilla JS, LocalStorage, Web Audio API)

```

## 📝 版本紀錄

* **v12 Final**: 優化 UI 玻璃擬態效果，整合番茄鐘與碎紙機功能。

---

*Created by [Your Name]*
