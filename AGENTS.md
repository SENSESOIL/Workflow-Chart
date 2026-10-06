# 部署指示（給本機 agent）

本 repo 只放拾壤流程圖的前端頁面，線上網址：https://sensesoil-workflow-chart.vercel.app

收到 `index(vN).html` 時，不需詢問，直接：
1. 改名為 `index.html`，覆蓋 repo 根目錄的同名檔。
2. `git add index.html && git commit -m "流程圖 vN"`
3. `git push origin main`（Vercel 會自動部署，約 30 秒）

規則：
- `index.html` 是打包產物，已內嵌所有 JS／CSS，不要手動重構或格式化。
- 不要在 repo 內放資料檔；流程資料存在 Supabase `public.workflow_doc`。
- `vercel.json` 不要改，除非 APP 網域變更。
