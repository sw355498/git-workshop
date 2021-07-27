# Git學習筆記

### Git基本安裝及設定 

1. 確認git安裝及版本
```bash=
$ git --version
```
[git](https://git-scm.com/)
[Sourcetree](https://www.sourcetreeapp.com/)

2. 設定環境變數

```bash=
#設定使用者名稱
$ git config --global user.name "使用者名稱"

#設定使用者email
$ git config --global user.email "使用者email"

#確認設定的情況
$ git config --list

#git的設定檔
$ cat ~/.gitconfig
```

-----------------------------

### 建立 repo

1. 建立資料夾
```bash=
$ mkdir 資料夾名稱
```
2. 進入該檔案夾
```bash=
$ cd 資料夾路徑(可拖曳資料夾至Git Bash)
```
3. 初始化 git 專案
```bash=
$ git init
```
4. 檢查看看是否有建立 .git 檔案夾
```bash=
$ ls -al
```

-----------------------------