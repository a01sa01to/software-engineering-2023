# Git Tutorial

## Git の流れ

1. リポジトリを作成する
2. Clone する
3. ファイルを編集する
4. Add する
5. Commit する
6. Push する

## Git の初期設定

```bash
git config --global user.name "NAME"
git config --global user.email "EMAIL"
```

## .gitignore

Git で管理しないファイルを指定する。
glob パターンで指定、コメントは `#`。

## Branch

共同作業するにあたって、作業を分けるために作る。
最終的には main に Merge する。

```bash
git branch # ブランチの一覧を表示
git branch BRANCH_NAME # ブランチを作成
git checkout BRANCH_NAME # ブランチを切り替える
git merge BRANCH_NAME # ブランチをマージす
git branch -d BRANCH_NAME # ブランチを削除する
```

## Conflict

同じファイルを編集して Merge したときに起きることがある。
Stash して Pull してから、Stash を戻して、 Merge する。

```bash
git stash
git pull
git stash pop
```

マージを中止する場合は、`git merge --abort` を実行する。

## GitHub Flow

GitHub Flow では、 main ブランチと dev ブランチの2つのブランチを使う。
開発は、 dev ブランチで行い、 main ブランチに Merge する。
リリースは main ブランチで Tag をつけて行う。
Hotfix は dev ブランチで行い、 dev ブランチで Tag をつける。
