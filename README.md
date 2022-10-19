# zcl1225
●/：根目錄，所有檔案皆從根目錄開始，只有root使用者具該目錄的許可權
●/root：該目錄為系統管理員，也稱作超級許可權者的使用者主目錄
●/bin：存放著經常使用的命令
●/boot：系統啟動時必須讀取的檔案,包括系統核心
●/home：存放普通使用者的家目錄，每個使用者都有自己的家目錄
●/etc：放置與系統設定、管理相關的檔案
●/usr：這是一個非常重要的目錄，使用者的應用程式和檔案都放在這個目錄下，類似與windows下的program files目錄
●/media：可用來做為光碟、軟碟片、隨身碟與其他分割區的自動掛載點
●/tmp：供全部使用者暫時放置檔案的目錄
●/var：系統執行時,內容經常變動的資料或暫存檔(log file),都會放置在這個目錄裡
●gzip
○壓縮：gzip FileName
○解壓縮：■gunzip FileName.gz■gzip -d FileName.gz8
xz○壓縮：xz -z FileName○解壓縮：xz -d FileName.xz●tar.gz○壓縮：tar -zcvf FileName.tar.gz DirName○解壓縮：tar -zxvf FileName.tar.gz9
find ■-size EX：找出大於500M的檔案→ -size +500M■-name EX：找出為照片的檔案→ -name "*.jpg"■-type EX：-type f→ 一般檔案;  -type d→ 一般目錄■-user EX：同時找兩個擁有者的檔案→-user user1 -o -user user210
●which filename○-a：系統會顯示所有被找到的命令執行檔之完整路徑○-n<文件名長度>指定文件名長度，指定的長度必須大於 或等於所有文件中最長的文件名。○-p<文件名長度>與-n参數相同，但此處的<文件名長度>包括了文件的路徑。○-w：指定輸出欄位 的寬度。○-V：顯示版本訊息。
●cat從第一行 顯示檔案內容、形成新檔案○cat -n file1 > file2→把file1的檔案內容加上行號後輸入file2檔案■-n  → 由1開始對所有輸出的行數編號■>    → 將多個文件覆蓋到目標文件中■>>  → 將多個文件追加到目標文件中，不覆蓋
●tac從最後一行 開始顯示○tac -r -s 'x\|[^x]' test.log→一個 接著  一個字符的反轉一個文件■-r→將分 隔符  作為基  礎正規表達是處理■-s→使用String作為分 隔符代替默認的換行符
●more一頁一頁的顯示  檔案內容○more +20 testfile→從第20行開始顯示testfile的文檔內容■EN TER：向下n行(default為1行)■Ctrl+F   /S PACE：向下滾動  一屏■Ctrl+B：返回上一 屏
●less與more類似，顯示檔案室允許用戶既可以 向前又可以向後翻頁閱讀檔案○ps -ef    |less→ps查看進程 信息並通 過less分頁顯示■j→下一行■k→上一行■G→移動  到最 後一行■g→移動  到第一行
●head 取出前面幾行(預設10行)○-n：後面接數字，代表幾行的意思
●tail 取出後面幾行(預設10行)○-n：後面接數字，代表幾行的意思○-n +20：只想列出20行以後的資料
●延遲（Latency）：封包從來源端至目的端中間所花的時間
●頻寬（Bandwidth）：傳輸媒介的最大吞吐量
●propagation delay：封包在網路線上傳輸所花費的時間，與網路 線上電 子訊號跑的速度有關，這個時間就是距離除以訊號傳送速度所得到的數值。
●transmission delay：網路 卡將資料傳送到網路線上所花的時間，與網路設備的傳送速度有關。
●nodal processing delay：路由器處理封包表頭、檢查位元資料錯誤與尋找配送路徑等所花費的時間。
●queuing delay：路由器因為某些因素無法立刻將封包傳送到網路上，造成封包暫存在佇列中等待的時間。
●netstat
●查看端口是否被占用：netstat -al grep 3306
●查看數據包統計信息：netstat -s
●查看路由信息：netstat -r
