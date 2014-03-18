git-starter
===========

## How to start a git for a beginner

### create remote repository (not use github)

```
### リモート側（pullされる方）
# ディレクトリ作成
$ mkdir -p /path/to/work/repo.git
# ディレクトリ移動
$ cd /path/to/work/repo.git
# bareリポジトリ作成
$ git --bare init --shared

### ローカル側 (pullする方)
# 作業ディレクトリ移動
$ cd /path/to/work
# リモート側からcloneしてファイルを持ってくる 
$ git clone /path/to/repo.git git_local

Cloning into 'git_local'...
warning: You appear to have cloned an empty repository.
done.
# ↑ bareレポジトリの中身が空だったよ警告 気にせず進める

# ディレクトリ作成
$ cd git_local
# 適当なファイルを作成
$ touch README.md 
# git 管理にファイルを追加
$ git add .
# 作業確定 
$ git commit -m "first commit"
[master (root-commit) 84c406d] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

# ローカル側からリモート側にファイルをpush
$ git push
Counting objects: 3, done.
Writing objects: 100% (3/3), 209 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To /path/to/work/repo.git
 * [new branch]      master -> master

```