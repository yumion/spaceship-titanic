# spaceship-titanic
https://www.kaggle.com/competitions/spaceship-titanic/overview

## ディレクトリ構成
```
dataset/  # データセット
|- train.csv
|- test.csv
|- sample_submission.csv
src/ #  ソースコード
|- notebook/  # jupyter notebook
|- hoge.py  # 実行用ファイル
submit/  # 提出用フォルダ
|- 20220523_lgbm_submit.csv  # 日付とモデル・特徴量を書く
```

## git運用
### gitブランチ戦略
- GitHubフローを基に以下運用方針を作成

#### 各ブランチの役割
|ブランチ|役割|
|---|---|
|main|成果物用|
|develop/merging|内部統合用|
|feature/${機能名}|個別機能開発用|

※PullRequestは1つ上のブランチに対して行う  
`feature`/`${機能名}` → `develop`/`merging` →`main`

#### 作業中の注意事項
- 作業準備
  - [Gitのインストール](https://gitforwindows.org/)(optional)
  - [Forkのインストール](https://git-fork.com/)(optional)
  - `git clone https://github.com/yumion/spaceship-titanic.git`をターミナルで実行
- 作業前
  - `git fetch`, `git pull`コマンドを実施し、ローカルリポジトリを最新化する
- 作業中
  - 1つの関心事(xxモデルの作成や~~バグの修正)が完了したら`git commit`でリモートリポジトリに更新を反映する
- コンフリクト発生時
  - ForkなどのGUIツールもしくはローカルファイルを確認し、反映したい変更を選択する
- 作業後
  1. `git status`コマンドでローカルリポジトリの状態を確認する
  1. `git add .`コマンドでローカルの変更を取り込む
  1. `git commit -m "メッセージを記載"`コマンドでメッセージを記載しコミット
  1. `git push`コマンドでリモートリポジトリにPush
  - `git Push`する前に必ず動作確認を行い正常に動作する事をチェックする
  - Descriptionは最低限レビューワーが理解できるように記載する
  - ファイルをリネームする際は`git mv`コマンドを利用し変更をトラッキングできるようにする
