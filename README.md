# git commands

## 工作区

```bash
touch firstFile.md
touch README.md

git status    # Untracked files

git add . # （vscode "stage all files") 工作区保存到暂存区

git status    # staged changes

git reset HEAD <file> # unstage/untrack file 从暂存区移除文件到工作区, git add <file> 相反命令（vscode STAGED CHANGES "-")

git reset HEAD # 从暂存区移除所有文件, git add . 相反命令（vscode "Unstage all files")
```

## 暂存区

If I change staged file (firstFile.md), the changed file is modified. 2 options:

> 一定是修改了暂存区文件后才能发生以下两个命令，分别是对新修改的接受和否定

```bash
git add .   # 暂存区状态a，修改该文件，并把最新的修改保存，更新暂存区里那个文件 (vscode CHANGES "+")

git checkout -- <file>  # to discard last change, 暂存区状态a，修改该文件，此命令撤销小改，回到状态a。(vscode CHANGES "revert sign")
git checkout -- .  # to discard all modified changes for all files, 暂存区状态a，修改该文件，此命令撤销小改，回到状态a。(vscode "discard all changes")
```

## 版本库

### commit staged files

```bash
git commit -m 'first commit'

# if previous commit is missing something, or message is wrong. Still that commit, not creating a new commit
git commit --amend  # press "i" to insert mode, press "esc" to quit insert mode, ":wq" to quit vm
git commit --amend -m 'first commit directly'

git log # review commits
```

### remote

```bash
git push origin master
```