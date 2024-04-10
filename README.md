# Git Practice note!
![alt text](image-1.png)
```c
$ git status
// 觀看目前資料夾狀態

$ git add .
// 將所有檔案加入暫存區

$ git commit -m "git init"
// 將暫存區的檔案進行 commit，-m 後面為 commit 的訊息

$ git commit --amend -m "git init again"
// 修改最後一次 commit 的訊息

$ git commit --amend --no-edit
// 將暫存區的檔案併入最後一次 commit

$ git log
// 查詢所有 commit 紀錄

$ git log -p
// 參數 -p 顯示 commit 詳細資訊

$ git log --oneline --graph
// 參數 --oneline 顯示更精簡的 commit 紀錄
// 參數 --graph 顯示 commit 線圖

$ git log --all
// 參數 --all 顯示包含 branch 的紀錄
```
```c
$git remote add origin https://github.com/jeremy900425/Git-Practice-note.git
//把本地端的資料夾連線到github的repo。不一定要叫origin

$git push origin master
//就是把你的master branch推上origin <origin就是你的github repo>
$git push -u origin master
//-u：代表把預設的remote設定成origin 未來push如果不指定remote都會推到origin

//所以說只要用過$git push -u origin master之後都只要打git push就好
```

```c
$git reset -- <檔案名稱>
//把add的檔案移除，因為commit只會推上有add過後的檔案

$git checkout -- <檔案名稱>
//pull後 對A檔案做了修改，想要恢復成原本pull下來的狀態就使用這個指令 #要先unstage

$git reset --soft HEAD~1
//如果commit訊息打錯了，可以回覆一次（~恢復幾次）
```

## conflicts概念
A修改一段訊息“大象會飛”並且已經commit並推上github了
此時，B還沒有git pull，把“大象會飛”改成“你還好嗎”，此時直接push就會出錯，因為B並沒有把最新的檔案pull下來
但是當B執行pull的時候，git會自動偵測到衝突的地方，如下圖所示
![alt text](image.png)，如果用vscode就可以直接按Accept Current Change選擇自己的內容，如果兩個都是你要的可以先按both那個再自己手動修改