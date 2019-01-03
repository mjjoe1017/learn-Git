
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
