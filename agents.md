# teaching-exam-skills（專案藍圖）

> 本檔為跨 Agent 通用的專案藍圖（AGENTS.md 開放標準）。任何 Agent 的每個 session 都應先讀本檔＋`handoff.md`。

## 專案簡介
一組可重用的 Agent Skills，專注於國中數學段考命題、審題、幾何配圖（SVG 渲染）與形成性評量小遊戲的繁體中文教學輔助工具集。

## 關鍵時程
- 2026-07-15：將預設分支切換為 main，完成康軒課綱 references 檔名與內文同步
- 2026-07-22：對齊最新 project-init 規範，調整 Obsidian 專案駕駛艙筆記位置與檔名 (`teaching-exam-skills/專案工作流程.md`)

## 目標與路線圖
- [x] 階段一：建立段考命題 (`jh-math-exam`)、情境非選 (`jh-math-context-questions`)、幾何配圖 (`jh-math-geometry`) 與評量遊戲 (`teaching-minigames`) 四項 Agent Skills
- [x] 階段二：切換預設分支至 `main` 並完成課綱單元命名與 references 檔名同步
- [x] 階段三：根據最新 project-init 規範，調整 Obsidian 專案駕駛艙筆記檔名與位置（`teaching-exam-skills/專案工作流程.md`），並升級專案至 L3 三層級架構
- [ ] 階段四：持續優化數學試題生成 prompt 範本與幾何 SVG 圖像品質

## 資料夾結構
- `README.md`：專案說明文件
- `LICENSE`：MIT 開源授權條款
- `.gitignore`：Git 忽略清單
- `skills/`： Agent Skills 核心邏輯
  - `jh-math-exam/`：段考命題與審題技能
  - `jh-math-context-questions/`：情境素養非選擇題生成技能
  - `jh-math-geometry/`：幾何命題與 SVG 配圖技能
  - `teaching-minigames/`：形成性評量小遊戲生成技能
- `agents.md`：專案藍圖（本檔）
- `handoff.md`：交接檔

## 同步層級（本專案初始化至第 3 層級）

| 層級 | 平台 | 位置 | 讀取時機 |
|------|------|------|---------|
| L1 | 本地（GDrive） | `agents.md`＋`handoff.md` | 每個 session |
| L2 | GitHub | changyiwu/teaching-exam-skills | 指定時 |
| L3 | Obsidian | teaching-exam-skills/專案工作流程.md | 有需要時 |

## 三個檔案的職責（依「時效性」分家，不是依「詳細程度」）

| 檔案 | 時效 | 寫入方式 | 放什麼 |
|------|------|---------|--------|
| `handoff.md` | **只對下一個 session 有效**，過期即丟 | 每次收工整份重寫 | 做到哪、下一步、**這次**的暫時 workaround |
| `agents.md`（本檔） | **長期有效**，每個 session 都適用 | 只有規則本身變了才改 | 目標、路線圖、常設規則、結構 |
| Obsidian／`git log` | **歷史**：發生過什麼、為什麼 | 只增不刪 | 決策紀錄、踩坑完整版、逐次進度 |

驗收標準：**`handoff.md` 整份刪掉，不應損失任何長期資訊**——會的話代表該升級進本檔卻沒升級。

**本檔不要出現的東西**：❌ `## 最近進度`／逐次工作紀錄、❌ 決策理由與踩坑完整版。歷史寫 L3 筆記的〈🗓️ 最近更動紀錄〉〈🧠 決策紀錄〉〈🕳️ 踩坑筆記〉；踩過的坑只把**結論**收斂成一條祈使句寫進〈工作約定〉，原因留 L3。

## 工作約定
- 任何 Agent、任何電腦：**開工先讀 `handoff.md`，收工必更新 `handoff.md`**
- 修改共用檔案前先讀最新內容，避免覆蓋其他 Agent 的變更
- 所有回應與文件使用繁體中文；涉及檔案操作時回報完整產出位置
- Windows 指令優先使用 PowerShell 語法
- 修改前先確認計畫，優先保留原有資料結構
- 不把每日流水帳寫進本檔

## 安全與隱私

- 不要 commit API key、token、密碼或 Firebase Admin 憑證
- 不要 commit 學生真名；正式資料只使用班級代號與座號
