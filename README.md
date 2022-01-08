# 1. 実装したい機能をissueに記載する  
1.  今、どんな状況？
2.  今後、どうしていきたい？
3.  何を使う？  


# 2. main を最新のバージョンに更新
#### main branch にいることを確認
    git branch
#### 変更されているファイルが無いか確認
    git status
#### main branch を最新のバージョンに更新
    git pull origin main  
    
    
# 3. branch を切って作業
#### 「-b」をつけると、ブランチを作成すると同時にそのブランチに移動する。isuue番号をbranch名に含める。
    git checkout -b back-btn#27
#### 変更したファイルの一覧を確認
    git status
#### 差分の確認
    git diff
#### ステージする
    git add .
#### isuue番号を含めてcommit
    git commit -m “back-btn#27”  
    
    
    
# 4. main を最新のバージョンに更新
#### チームメンバーがリモートリポに変更を加えている可能性があるため、プッシュする前に必ずリモートリポのmainをPullする
    git pull origin main
#### 本来ならここでコンフリクトする可能性があるので、その場合は修正して再度 add & commit
    git add . & git commit


# 5. push して pull request を作成し、mainにmergeする
#### HEADを使えば、ブランチ名を指定しなくてもカレントブランチをリモートにpushすることができる。
    git push origin HEAD
#### pull request の作成
#### このタスクを完了する場合は、詳細に『close#番号』を書く。これでissueが自動的にタスク完了と見なして、処理してくれる。
    close #27
#### ブランチでの作業終了後にリモートリポでプルリクエストをmainにmergeする  
    merge


# 6. localのmainを更新して、branchを削除する
#### main に戻る
    git checkout main
#### mainを最新のバージョンに更新
    git pull origin main
#### branchの削除
    git branch -d back-btn#27
    
    
# 6. 便利コマンド
#### logの表示(branchの場所が分かる)
    git log --oneline --decorate
