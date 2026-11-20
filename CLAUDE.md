# Casevoras 異常矯正工作台（Casevora-CAPA）

- 網址版：GitHub 倉庫 `NUVYROTH/Casevora-CAPA` 的 `main` → https://nuvyroth.github.io/Casevora-CAPA/
- 原始檔只有一份：`index.html`。

## 上線流程（擁有者要求：一定要先給預覽）

1. 一律在固定的 `preview` 分支修改並推上去（`git checkout -B preview main`），不要直接改 `main`。GitHub Pages 只發布 `main`，所以推 `preview` 不影響網站。
2. 用假資料測試（例：王小明、作業員 A、測試品項），電腦與手機尺寸都測。
3. **上線前一定要先給擁有者預覽**：把 `index.html` 發布成私人預覽頁（claude.ai Artifact）給擁有者實際操作，並附截圖。
4. 擁有者回覆「可以上線」後，才 `git push origin preview:main`。沒有這句話不能合併到 `main`。

## 不能改變的原則

- 程式碼裡不能有任何金鑰（API key、`service_role` 等）。
- 誠實文案「本機儲存 · 僅在此裝置此瀏覽器有效 · 無登入權限控管 · 請勿用無痕視窗 · 定期下載備份」不能拿掉。
- 版面與 LOGO 要跟衛生追蹤（Casevora-Inspect）、文件追蹤（Casevora-CertTrack）一致。
- 每個分頁都要有使用說明（`guideBox`）；功能改動時要同步更新說明文字。
- 清單表頭、編輯表單的欄名與順序要跟擁有者的 Excel 一樣：案件編號、發現日期、工作站、品項、廠商、批號、效期、異常、圖片(1)、圖片(2)、備註、處理辦法、結案日期、分類一、分類二；只多「預計完成日期」（預設發現日期＋15 天）。
- 匯入 Excel 只會新增，不覆蓋；案件編號重複或內容完全相同的略過。
- 不在表單上的舊欄位資料要保留（唯讀顯示在「其他（舊欄位）」）。
- 測試、截圖一律用假資料，不要把擁有者的真實案件內容貼到外部。
