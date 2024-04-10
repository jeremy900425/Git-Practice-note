# Git Practice note!
https://ithelp.ithome.com.tw/upload/images/20190227/20115569eeG008szA0.png

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