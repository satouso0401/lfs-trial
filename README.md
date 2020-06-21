Git LFS を試してみる
====================

クライアント側でgit-lfsのインストールが必要
```
brew install git-lfs
git lfs install
```

lfs track コマンドでLFSで管理したいファイルを指定する

```
git lfs track "path/to/file/*"
```
.gitattributes ファイルができるのでそのファイルを直接手で編集しても良いかもしれない


あとは通常通り commit, push すればLFSで管理してくれる

```
lfs-trial $ git push
Uploading LFS objects: 100% (1/1), 781 B | 0 B/s, done.                                                                                                                                                                                                                  
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 825 bytes | 825.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/satouso0401/lfs-trial.git
   5b6e87d..7545601  master -> master
```


git-lfsをインストールしていないクライアントがいるとおかしな事になるらしいので、チームで開発する際はみんなインストールする。
https://medium.com/nttlabs/enabling-git-lfs-c907ca393ccb


