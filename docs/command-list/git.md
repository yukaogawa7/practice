# Git Commands

### 【作業の進め方】  
１．git cloneしてローカルにリポジトリを落としてくる
　　⇒リモートリポジトリがない状態で、最初にローカルリポジトリを作るときは、git init  
２．git branchでブランチを作り、git checkoutでブランチを移動して、その中で編集作業をする  
３．git addしてcommitでローカルリポジトリを保存  
４．git pushでリモートレポジトリを更新  

## git init
⇒ローカルリポジトリを新規作成する  
　削除したい場合：rm -fr .git  
**リポジトリとディレクトリの違い**  
　リポジトリ：ファイルやディレクトリなどの変更履歴を格納する場所  
　ディレクトリ：作業ファイルを格納する場所  
## git add
⇒コミットする前に、ステージングエリアにファイルを追加する  
  git add （フルパス）  
  追加したファイルをステージングエリアから戻す場合：git reset (./ファイル名)  
## git commit
⇒リポジトリに変更した内容を保存すること  
  git commit -m "コメント"  
  *commitを取り消したい場合：git reset (取り消したいコミットID)  
  *commitのみ取り消し：git reset --soft  
  *commitとaddの取り消し：git reset --mixed もしくはオプションなし  
  *全取り消し：git reset --hard  
  *全取り消し自体取り消し：git reflog  
## git status
⇒現在作業しているプロジェクトのファイル状態を確認する 
　*ステージングエリアに追加したファイル：「Changes to be committed:」配下  
　*変更したファイル：「Changes not staged for commit:」配下  
　*新規追加したファイル：「Untracked files:」配下  
## git log
⇒コミットした履歴を確認する  
## git push
⇒ローカルリポジトリのコミット履歴をリモートリポジトリに送信して更新する  
  git push origin (ブランチ名)  
## git branch
⇒ブランチの一覧が表示される  
　ブランチを新規作成する：git branch (新規ブランチ名)  
　ブランチ：分岐して履歴を記録する。同じリポジトリで複数の変更を平行して進めることができる  
           最初にブランチを作って、そこで作業する。mainは触らない。  
## git checkout
⇒ブランチを切り替える  
## git fetch
⇒リモートリポジトリの最新の履歴を取得する  
## git merge
⇒変更をカレントブランチに統合する  
## git pull
⇒リモートリポジトリの履歴を取得する  
　fetchしてmergeしている  