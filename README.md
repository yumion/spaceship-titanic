# spaceship-titanic
https://www.kaggle.com/competitions/spaceship-titanic/overview

## gitブランチ戦略
- GitHubフローを基に以下運用方針を作成

### 各ブランチの役割
|ブランチ|役割|
|---|---|
|main|成果物用|
|develop/merging|内部統合用|
|feature/${機能名}|個別機能開発用|

※PullRequestは1つ上のブランチに対して行う  
`feature`/`${機能名}` → `develop`/`merging` →`main`

### 作業中の注意事項
- GitへPushする前に必ず動作確認を行い正常に動作する事をチェックする
- Descriptionは最低限レビューワーが理解できるように記載する
- ファイルをリネームする際は`git mv`コマンドを利用し変更をトラッキングできるようにする
