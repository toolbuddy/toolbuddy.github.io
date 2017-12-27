---
layout     : post
title      : "papoGen 0.0.16 - Release note"
subtitle   : "Node.js Modules"
date       : 2017-12-27 18:00:00
author     : "Toolbuddy"
tags       : papoGen WebGenerator JSON Markdown NodeJS PaperCSS Pug
comments   : true
signature  : true
slides     : 
present    : 
---

![papoGen](https://i.imgur.com/ts1PC5b.png)

> **papoGen `0.0.16`** Release - 目前穩定支援的版本。
> 支援 macOS 與 Linux 系統上的 Node.js，只要透過 `npm install -g papoGen` 即可立即體驗！

## About papoGen `0.0.16`

* 支援 macOS 與 Linux 系統上的 Node.js，為目前穩定支援版本。
* 支援 JSON/YAML 檔案格式作為輸入。
* 透過以下三種模組進行網頁生成：
    1. 使用者自訂 Pug 樣板
    2. 使用者自訂 JSON / YAML 網頁內容
    3. 使用者或第三方自訂 CSS 模板

### papoGen `0.0.16` Workflow

![]({{ site.baseurl }}public/workflow.png)

**papoGen `0.0.16`** 是目前穩定支援版本，支援 macOS 與 Linux 系統上 Node.js 的使用。
**papoGen `0.0.16`** 新增 YAML 檔案格式輸入，而 YAML 的撰寫規格與 [JSON 的規格]((https://github.com/toolbuddy/papoGen/tree/master/test/json)) 相同，只有將與法改為 YAML。另外，使用者也可以透過 `papogen` 指令來建立 script template 來做修改後使用！可以參考這篇 [使用方法](https://github.com/toolbuddy/papoGen/blob/master/example/README.md#generate-script-template-by-command)。
**papoGen `0.0.16`** 支援以下二種輸出樣式： `doc` 與 `resume`，以下為操作指令！
```
papogen -s <裝有剛剛編輯文檔的目錄> -o <網站產生的目錄> -g <使用的文檔格式，ex: json or yaml> -m <想要使用的網站 template，ex: doc or resume> -t <網站 title>
```
這麼一來就可以看到產生的網站囉！

### Bonus

* 在圖片 (`image`) 與程式區塊 (`code`) 的規格中，檔案來源支援 **相對路徑**！
* 關於圖片 (`image`) 規格
papoGen 會自動將圖片檔案複製到輸出資料夾的 `res/` 底下做使用，另外也支援 **圖檔網址** 作為圖檔來源，你可以直接提供圖檔的網址作為參數使用。
* 關於程式區塊 (`code`) 規格
papoGen 會在讀取完畢程式碼後直接嵌入網頁中，無須擔心檔案相對路徑問題！

### Conclusion

* 歡迎貢獻！
* 覺得有趣的話，也希望可以給顆星星~

---
## References

* [papoGen GitHub](https://github.com/toolbuddy/papoGen)
* [papoGen DEMO](https://toolbuddy.github.io/papoGen/)
    * [papoGen DEMO - doc](https://toolbuddy.github.io/papoGen/doc)
    * [papoGen DEMO - resume](https://toolbuddy.github.io/papoGen/resume)
* [Previous papoGen introduction](https://toolbuddy.github.io/2017/12/18/papoGen/)

---
## Contact

* [Kevin Cyu](https://kevinbird61.github.io/Intro/)