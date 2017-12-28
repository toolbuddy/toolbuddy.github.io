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

## About papoGen 0.0.16

* 支援 macOS 與 Linux 系統上的 Node.js，為目前穩定支援版本。
* 支援 JSON/YAML 檔案格式作為輸入。
* 透過以下三種模組進行網頁生成：
    1. 使用者自訂 Pug 樣板
    2. 使用者自訂 JSON / YAML 網頁內容
    3. 使用者或第三方自訂 CSS 模板

### 1. papoGen `0.0.16` Workflow

![]({{ site.baseurl }}public/workflow.png)

**papoGen `0.0.16`** 是目前穩定支援版本，支援 macOS 與 Linux 系統上 Node.js 的使用。
**papoGen `0.0.16`** 新增 YAML 檔案格式輸入，而 YAML 的撰寫規格與 [JSON 的規格]((https://github.com/toolbuddy/papoGen/tree/master/test/json)) 相同，只有將與法改為 YAML。另外，使用者也可以透過 `papogen` 指令來建立 script template 來做修改後使用！可以參考這篇 [使用方法](https://github.com/toolbuddy/papoGen/blob/master/example/README.md#generate-script-template-by-command)。
**papoGen `0.0.16`** 支援以下二種輸出樣式： `doc` 與 `resume`，以下為操作指令！
```
papogen -s <裝有剛剛編輯文檔的目錄> -o <網站產生的目錄> -g <使用的文檔格式，ex: json or yaml> -m <想要使用的網站 template，ex: doc or resume> -t <網站 title>
```
這麼一來就可以看到產生的網站囉！

### 2. Example usage (詳細版)

以下展示了如何透過 papoGen 來快速產生一個網站：
* 編輯 `src/` 內的 JSON / YAML 檔案。
* 運行指令即在資料夾 `out/` 下生成結果網頁。

#### 2.1 Get Started

* 透過 npm 安裝 `papogen`。
    ```bash
    » [sudo] npm install -g papogen
    ```
* 編輯 `src/` 內的 JSON 檔案，每個 JSON 檔案代表一種類型，詳細察看根目錄中 `test/README.md`。
* 運行指令產生：以下 `-s`,`-o` 為必備之外，其餘的參數指定都有預設值！
    ```bash
    » papogen -s src/ -o out/ -t <your title> -m <model you want> -g <support format>
    ```
* 範例：使用 YAML 生成
    ```bash
    » papogen -s test/yaml -o docs/resume-yaml -g yaml -m resume -t papoGen-YAML
    ```

#### 2.2 Generate Script Template by Command

* 在 **papoGen `0.0.12`** 版開始，可以支援透過 `papogen` 產生可支援的腳本格式。
* 利用 `papogen -h` 來列出有支援哪些後，便可以利用 `<script>`（**藍色**部份）以及 `<format>`（**灰色**部份）的組合，來產生腳本；組合方式： `<script>` / `<format>`
    ```bash
    ~/develop » papogen -c json/text -o

    Welcome using toolbuddy@papoGen!
    Current version: 0.0.12

    - src is %s /usr/local/lib/node_modules/papogen
    - out is %s
    - title is %s Power by papoGen
    - gen is %s json
    - model is %s doc


    Generating ...
    Specified: json/text
    Output dir(for script template):
    [Success] Write script template file - json/text
    ```
* 在 **papoGen `0.0.12`** 開始支援多個 `<format>` 的指定，可以一行指令生成多個模板 !
    ```
    ~/develop » papogen -c json/text/list/table -o .
    ...
    # 生成 text.json, list.json, 以及 table.json
    ```
* 在 **papoGen `0.0.12`** 開始也支援全部 `<format>` 的指定（每種各一個）
    ```
    ~/develop » papogen -c json/all -o .
    ...
    生成全部的 template ！
    ```
#### 2.3 Help Manual

* 如有任何使用疑問，可以下 `-h` 的參數做察看
    ```bash
    » papogen -h
    ```

### 3. Bonus

* 在圖片 (`image`) 與程式區塊 (`code`) 的規格中，檔案來源支援 **相對路徑**！
* 關於圖片 (`image`) 規格
papoGen 會自動將圖片檔案複製到輸出資料夾的 `res/` 底下做使用，另外也支援 **圖檔網址** 作為圖檔來源，你可以直接提供圖檔的網址作為參數使用。
* 關於程式區塊 (`code`) 規格
papoGen 會在讀取完畢程式碼後直接嵌入網頁中，無須擔心檔案相對路徑問題！

### 4. Conclusion

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