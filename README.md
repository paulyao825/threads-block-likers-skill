# threads-block-likers-skill

一個 Claude Cowork 技能，透過瀏覽器在你自己已登入的 Threads 帳號上，封鎖某則貼文或留言底下所有按讚的人。

## 使用前準備（Cowork 環境設定）

這個技能是靠「**Claude in Chrome**」瀏覽器擴充功能來操作 Threads 網頁（不是單純的桌面畫面控制 / Computer Use）。第一次使用前，請先完成：

1. 用 Google Chrome 瀏覽器（暫不支援其他 Chromium 分支瀏覽器或手機版）。
2. 到 Chrome 線上應用程式商店安裝「Claude」擴充功能，並登入你的 Claude 帳號。
3. 在 Claude 桌面版／Cowork 裡打開「設定 → 連接器（Connectors）」，找到 **Claude in Chrome**，把它打開。
4. 在對話視窗上方的「Connectors」下拉選單中，針對這次對話手動啟用 Claude in Chrome（它預設關閉，每次新對話都要開一次）。
5. 在該瀏覽器中先自行登入要操作的 Threads 帳號。

沒完成以上設定的話，Claude 沒辦法打開瀏覽器分頁、讀取網頁內容或點擊按鈕，這個技能就無法執行。

## 下載

- **最簡單：** 點擊上方的 `threads-block-likers.skill`，再用該檔案頁面上的「Download raw file」（下載圖示）按鈕下載。
- 或直接複製整個 repo：`git clone https://github.com/paulyao825/threads-block-likers-skill.git`
- 或用上方綠色的「Code」按鈕，選擇「Download ZIP」。

## 安裝到 Claude Cowork

1. 從這個 repo 下載 `threads-block-likers.skill`。
2. 把它丟進 Claude Cowork 的聊天視窗，或打開後點擊「Save skill」按鈕（如果你的工作環境支援這種安裝方式）。
3. 安裝完成後，直接跟 Claude 說類似「幫我封鎖這則貼文所有按讚的人：<Threads 網址>」就可以了。

## 檔案說明

- `threads-block-likers.skill` — 打包好、可直接安裝的技能檔案。
- `threads-block-likers-SKILL.md` — 技能的操作指示（決定它實際行為的原始檔）。
- `threads-block-likers-USER_GUIDE_zh-TW.md` — 給非技術背景使用者看的繁體中文白話使用說明。

## 這個技能會做什麼

給定一則 Threads 貼文或留言的網址，這個技能會：

1. 打開該貼文的按讚名單（透過「查看動態」→「按讚內容」）。
2. 動手前先把完整名單列給你看，等你確認。
3. 以接近真人的節奏，一個一個從你自己的 Threads 帳號封鎖這些人。
4. 回報封鎖、略過或失敗的結果。

它只會處理你指定的那一則貼文/留言，絕對不會問你要密碼，也不會代替你解任何驗證碼。
