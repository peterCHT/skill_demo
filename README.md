# meeting-summary

這是一個最小可用的 Codex Skill demo，用來示範如何把一段會議逐字稿、零散會議筆記或站會更新，整理成結構化的會後摘要。

這個 skill 會把輸入內容整理成：

- 摘要
- 決議
- 待辦事項
- 風險與待釐清問題

## Demo 重點

這個範例刻意保持簡單，只包含一個 `SKILL.md`，不需要 API key、不需要額外腳本，也不需要任何外部依賴。適合用來展示：

- skill 的基本資料夾結構
- `SKILL.md` 的 frontmatter 寫法
- 如何用中文描述 skill 的觸發條件與工作流程
- 安裝後如何用 `$meeting-summary` 觸發 skill

## 資料夾結構

```text
meeting-summary/
  SKILL.md
  README.md
```

## 使用方式

安裝這個 skill 後，可以在 Codex 中輸入：

```text
Use $meeting-summary 整理這段會議筆記：

Alice 說登入頁本週五要上線。Bob 還在等設計稿。Carol 說 API 已經 ready。
決定先不上 SSO，留到下個 sprint。風險是 QA 時間只剩兩天。
Bob 要明天下午前補設計稿。
```

預期輸出會包含四個區塊：

```text
## 摘要

- 登入頁目標是在本週五上線。
- API 已經準備完成。
- 設計稿仍在等待 Bob 補齊。

## 決議

- SSO 先不上線，延到下個 sprint。

## 待辦事項

- Bob：補設計稿，明天下午前

## 風險與待釐清問題

- QA 時間只剩兩天，可能影響上線品質或時程。
```

## 設計說明

這個 demo 展示的核心概念是：Skill 不一定要包含複雜工具或程式碼。即使只有一份 `SKILL.md`，也可以把一套固定的工作方式封裝起來，讓 Codex 在類似任務中穩定地按照同一種格式與標準輸出。

## 建議 commit message

```text
Add meeting summary skill demo

- Add a minimal Chinese Codex skill for meeting note summarization
- Document the demo purpose, folder structure, and example trigger prompt
- Include expected output format for easier presentation
```
