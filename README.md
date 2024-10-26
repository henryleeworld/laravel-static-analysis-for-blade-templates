# Laravel 11 Blade 模板靜態分析

引入 tomasvotruba 的 bladestan 套件來擴增 Blade 模板靜態分析，可以對程式碼進行嚴格的語法檢測，儘量將程式碼執行錯誤率降到最低。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行二進位制檔案用於分析目錄並輸出遇到的任何錯誤。
```sh
$ ./vendor/bin/phpstan analyse {目錄，例如：resources}
```

----

## 畫面截圖
![](https://i.imgur.com/437Pq8x.png)
> 執行二進位制檔案檢查
