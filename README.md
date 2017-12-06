# git commands

```bash
touch firstFile.md
touch README.md

git status    # Untracked files

git add. # （vscode "stage all files")

git status    # staged changes

git reset HEAD <file> # unstage/untrack file 从暂存区移除文件, git add <file> 相反命令（vscode STAGED CHANGES "-")
git reset HEAD # 从暂存区移除所有文件, git add . 相反命令（vscode "Unstage all files")

# If I change staged file (firstFile.md)
# The changed file is modified. 2 options:

# 一定是修改了暂存区文件后才能发生以下两个命令，分别是对新修改的接受和否定

1) git add .   # 暂存区状态a，修改该文件，并把最新的修改保存，更新暂存区里那个文件 (vscode CHANGES "+")
2) git checkout -- <file> to discard last change   # 暂存区状态a，修改该文件，此命令撤销小改，回到状态a。(vscode CHANGES "revert sign")
```