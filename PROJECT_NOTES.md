# teaching-exam-skills 專案開發筆記

## 📌 當前進度與待辦事項
- [x] 修改 jh-math-exam SKILL.md 內引用之檔案名稱，使其與 references 資料夾一致
- [/] 初始化本地 Git 倉庫並關聯 GitHub 遠端倉庫
- [x] 建立專案規範 ANTIGRAVITY.md 與專案開發筆記 PROJECT_NOTES.md
- [/] 在 2ndbrain 建立專案駕駛艙並進行同步

## 📝 踩坑紀錄與解決方案
- **環境變數干擾**：Windows 環境下，環境變數 `GITHUB_TOKEN` 的無效值可能會使 `gh` 命令失敗。解決方法是在執行 `gh` 指令前，在 PowerShell 中執行 `$env:GITHUB_TOKEN=""`。

## 🎯 下一步規劃
1. 將新建立的專案規範與筆記檔案提交至 Git。
2. 推送變更至 GitHub 遠端倉庫。
3. 建立並同步 Obsidian 專案駕駛艙。
