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

## git語法

### 查看狀態：
```bash=
$ git status
```

### 把檔案從 工作目錄 加到 暫存區：
```bash=
$ git add 檔案名稱
```

### 提交暫存區的檔案到儲存庫(repo)：
```bash=
$ git commit -m "紀錄這次提交的緣由"
```

### 同時 add 跟 commit，只有針對已經 tracked 檔案才有效：
```bash=
$ git commit -am "紀錄這次提交的緣由"
```

### 查看紀錄：
```bash=
$ git log
```

### 比較檔案的差異(確認後，可以按 q 離開)：
```bash=
$ git diff
```

### 移除檔案：
    + 從 git 中移除，但是檔案還在
    ```bash=
    $ git rm {檔案名稱}
    ```

    + 從 git 中移除，且真的移掉檔案
    ```bash=
    $ git rm --cached {檔案名稱}
    ```

### 從暫存區域回到工作目錄：
```bash=
$ git restore --staged {檔案名稱}
```

### 捨棄在工作目錄的改變(包括修改與刪除)：
```bash=
$ git restore {檔案名稱}
```

### 建立分支與合併：
+ 檢視分支
    ```bash=
    $ git branch
    ```

+ 新增分支
    ```bash=
    $ git branch {分支名稱}
    ```

+ 切換分支
    ```bash=
    $ git switch {branch-name} 
    ```

+ 合併分支
    1. 先切換到要合併的分支
    ```bash=
    $ git switch {要合併的分支名稱}   (新)
    $ git checkout {要合併的分支名稱} (舊)
    ```
    2. 再把 要被合併的分支 合併進來
    ```bash=
    $ git merge {要被合併的分支名稱}
    ```
    
+ 刪除本地分支
    ```bash=
    $ git branch -d {要刪除的分支名稱}
    ```

-----------------------------

## 建立 github repo

### 增加一個遠端repo 的連結，這個遠端的名稱叫做 origin
```bash=
$ git remote add origin {url}

$ git branch -M main
```

### 設定 main 這個分支跟 origin 遠端的main 分支做連結且 push 上去
```bash=
$ git push -u origin main
```

### 設定 set-upstream 過後，就可以不用指定 origin {分支名稱}
```bash=
$ git push
```

-----------------------------