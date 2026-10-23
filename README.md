# 本丸家行程筆記 app
- 直接雙擊 index.html 即可使用(資料存在瀏覽器本機)。
- 想用通知 / PWA:執行「啟動.bat」(需 Python),或在此資料夾執行 `python -m http.server 8080`,開 http://localhost:8080
- 資料只存在該瀏覽器,請定期按「匯出」備份。
- 之後擴充手機:同一套檔案放到 HTTPS 主機(或區網+HTTPS),手機加到主畫面即可。

## 資料保存
1. 資料自動存在瀏覽器(localStorage)。建議用「啟動.bat」開 http://localhost:8080,網址固定資料才不會因搬動檔案而「消失」。
2. 在 Chrome / Edge 按上方「💾 存檔」→「建立存檔檔案」,選本資料夾,之後每次修改都會自動寫入該檔(本丸家行程資料.json)。重開瀏覽器可能需點一次「恢復檔案存取」。
3. 也可隨時按「匯出」下載備份,「匯入」或「開啟既有存檔檔案」還原。

## Android 手機版
**方式 A:PWA(最簡單)**
1. 把整個資料夾放到有 HTTPS 的免費主機(Netlify Drop、GitHub Pages、Cloudflare Pages 皆可)。
2. 手機 Chrome 開該網址 → 右上 ⋮ →「安裝應用程式」(或上方「📲 安裝」鈕)。主畫面會出現圖示,全螢幕、可離線使用。
3. 資料存在手機本機,不會上傳。

**方式 B:真正的 APK**
1. 完成方式 A 取得 HTTPS 網址。
2. 到 pwabuilder.com 貼上網址 →「Package for stores」→ Android → 下載 APK,傳到手機安裝(需允許未知來源)。

**手機注意**
- Android Chrome 不支援「綁定存檔檔案」,請定期按「匯出」(下載到手機)備份,必要時再「匯入」。
- 通知需先按「🔔通知」授權;PWA 在背景時 Android 可能延遲或不發提醒。
