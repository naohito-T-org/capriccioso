# Introduction


## How To Use?


## memo

GitHub の Contributions、いわゆる「草」は、この内の**AuthorDateを見て色付けを行っている。**

```sh
$ git log --pretty=fuller
commit 4a2f79d9c3f25070c366b6edd6e7e58cb67cc27e (HEAD -> develop, origin/main, origin/develop, main)
Author:     naohito-T <naohito.tanaka0523@gmail.com>
AuthorDate: Wed Oct 20 00:15:58 2021 +0900
Commit:     naohito-T <naohito.tanaka0523@gmail.com>
CommitDate: Wed Oct 20 00:15:58 2021 +0900
```

コミットする内容を作った著者 (Author) の日付と、
そのコミット情報を取り込んだ人 (Commiter) の日付を別々に持っているということ。


`$ git commit --amend`
コミットの上書きコマンド

```sh

# 以下コマンドを打つ
$ git commit --amend --date="Mon Jul 11 12:00:00 2016 +0900"
# エディタがひらかれる

```

## テスト内容

最初に現在時刻を一度push
↓
つぎに2016
↓
つぎに2020(ここらへんでおかしくなってきている)
↓
つぎに2018
↓
つぎに2017

## テスト手順

1. ファイルを編集する
2. `$ git add .`
3. `$ git commit -m "fix"`
4. `$ git commit --amend --date="Mon Jul 11 12:00:00 2020 +0900" -m "fix"`
5. `$ git push` これはdevelopにそのまま

Tue 19 Oct 2021 04:01:48 PM UTC
備考
変わったか確認
`$ git log --pretty=fuller`
