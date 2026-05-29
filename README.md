# RTnexen PPS Tool

**One-click Git Push / Pull / Status for KiCad PCB Editor**

一鍵 Git Push / Pull / Status，專為 KiCad PCB 工作流程設計，不需要開終端機。

由 [RT Next-Energy Systems](https://rtnexen.com) 開發。

---

## Features / 功能

| | English | 中文 |
|---|---|---|
| ↑ | **Git Push** — Stage, commit with message, and push in one click | 一鍵暫存、提交、推送 |
| ↓ | **Git Pull** — Pull latest changes with live output log | 即時顯示拉取進度 |
| ● | **Git Status** — View branch, uncommitted files, recent commits | 查看分支狀態與近期提交 |
| ⚙ | **Settings** — View and update GitHub remote URL | 直接修改 Remote URL |

**其他特色：**
- 即時 log 輸出 — 每個步驟都能看到 Git 在做什麼
- 非同步載入 — UI 立即開啟，不卡頓
- Windows 無終端機閃爍 — 所有指令靜默執行

---

## Requirements / 系統需求

- KiCad 7.0 or later（已在 KiCad 10.0 測試）
- Git 已安裝並加入系統 PATH
- Windows / macOS / Linux

---

## Installation / 安裝

### 手動安裝

1. 從 [Releases](../../releases) 下載最新版 zip
2. 解壓後將 `rtnexen_git_tools/` 資料夾複製到 KiCad plugins 目錄：

   **Windows:**
   ```
   C:\Users\<你的名字>\Documents\KiCad\10.0\scripting\plugins\
   ```
   **macOS:**
   ```
   ~/Library/Preferences/KiCad/10.0/scripting/plugins/
   ```
   **Linux:**
   ```
   ~/.config/kicad/10.0/scripting/plugins/
   ```

3. 開啟 KiCad PCB Editor
4. **工具 → 外部插件 → 重新整理外掛程式**

工具列會出現 ↑↓ 圖示，點擊即可使用。

---

## Usage / 使用方式

點擊 PCB Editor 工具列的 **RTnexen PPS Tool** 圖示（↑↓）。

### Git Push
1. 選擇 **↑ Git Push**
2. 確認變更的檔案清單
3. 輸入 commit message（或使用快速按鈕）
4. 點擊 **Push ↑**

### Git Pull
1. 選擇 **↓ Git Pull**
2. 確認拉取
3. 完成後關閉並重新開啟專案以載入更新

### Git Status
1. 選擇 **● Git Status**
2. 查看目前 branch、未提交變更、最近 8 筆 commit

### Settings / 設定
任何視窗右上角的 **⚙** 按鈕可查看或修改 GitHub remote URL。

---

## Customization / 自訂

用任何文字編輯器開啟 `git_runner.py`，修改以下內容後，在 KiCad 重新整理外掛程式即可套用：

```python
VERSION = "2.1.0"            # 版本號
APPNAME = "RTnexen PPS Tool" # 顯示名稱
```

Settings → About 的聯絡資訊：
```python
label="rtnexen.com  |  ryan@rtnexen.com"
```

---

## License

MIT License — 自由使用、修改與發布。詳見 [LICENSE](LICENSE)。

---

## About / 關於

**RT Next-Energy Systems**
[rtnexen.com](https://rtnexen.com)
