
# Git環境安裝
[Git下載](https://git-scm.com/download/mac) 或使用 [Homebrew軟體安裝Git](https://brew.sh/index_zh-tw.html) <br><br>

# Git設定
> 開啟終端機設定使用者、Email信箱 <br>
```
git config --global user.name "your name"
git config --global user.email "your email@gmail.com"
```
> 檢視目前的設定
```
git config --list
```
>Git設定縮寫
```
git config --global alias.co checkout == git co
git config --global alias.br branch == git br
git confug --global alias.st status == git st
git config --global alias.l "log --oneline --graph" == git l
git config --global alias.ls 'log --graph --pretty=format:"%h <%an> %ar %s"' == git ls
```

>常用命令列指令<br>

| Mac OS | Description |
| --- | --- |
| cd | 切換目錄 |
| pwd | 取得目前所在的位置 |
| ls | 取得目前的檔案列表 |
| mkdir | 建立新的目錄 |
| touch | 建立檔案 |
| cp | 複製檔案 |
| mv | 移動檔案 |
| rm | 刪除檔案 |
| clear | 清除畫面上的內容 |

<br>

# Git新增資料夾、檔案
```
cd /tmp - 切換至tmp目錄
mkdir newFolder - 建立 newFolder 目錄
cd newFolder - 切換至 newFolder 目錄
git init - 初始化 newFolder 目錄, 讓Git對newFolder進行版控
git st - 查詢newFolder目錄的狀態

echo "hello world, git" > welcome.html - 建立hello world, git內容，儲存為welcome.html檔案
```

> 檔案交給Git

git add welcome.html - 將檔案放置暫存區<br>
git add \*.html <br>
git add --all <br>
git commit -m "init commit" - 將存放暫存區的檔案放置儲存庫(Repository) <br>
git commit --allow-empty -m "space" - 空值commit <br>

> Git操作圖
![image](https://gitbook.tw/images/using-git/working-staging-and-repository/all-states.png) <br>

> 直接將檔案add、commit
```
git commit -a -m "welcome.html"
```
> 檢視Git紀錄
```
git log
commit bddsfrefffffffff4 (HEAD -> master)
Author: username <username@gmail.com>
Date:   Thu Jan 3 22:28:03 2019 +0800

    init commit
```
or
```
git log --online --graph
```
<br>

# 查找commit人名
```
git log --oneline --author="username"
git log --oneline --author="username\|username2" - 同時查找2個人
```

# 查找commit內容
```
git log --oneline --grep="handsomeboy"
```

# 查找commit檔案內容
```
git log -S "superman"
```

# 查找commit時間
```
git log --oneline --since="9am" --until="12am"
got log --oneline --since="9am" --until="12am" --after="2017-01"
```

# Git刪除檔案
```
rm welcome.html
git add welcome.html - 將此次的修改加入暫存區
git rm welcome.html
```

# 移除Git控管
```
git rm welcome --cached
```

# 變更檔名
```
mv welcome.html hello.html
git add --all
git st
```

# Git變更檔名(較快)
```
git mv index.html hello.html
git st
```

# 修改commit後的紀錄
```
git commit --amend -m "Superman" - 修改最後一次commit的內容
```

# commit後需再追加檔案
```
git add forgetCommitFile.html
git commit --amend --no-edit - --no-edit參數意思是我不要編輯commit訊息
```
