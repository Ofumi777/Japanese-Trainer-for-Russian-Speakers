# JLPT N4 短文読解

ロシア語訳・語彙表・採点・解説付きのオリジナル練習教材です。

## ファイル構成

- `index.html`：セット一覧（今後もこの名前を維持）
- `n4-reading-01.html`：第1セット（5問）
- `.nojekyll`：静的ファイルをそのまま配信するための空ファイル
- `README.md`：公開と追加の手順

各練習セットは外部依存のない単一HTMLです。一覧との移動には相対リンクを使っています。

## 初回公開

1. GitHubで公開用リポジトリを作成するか、公開先リポジトリを開きます。
2. このフォルダーの中身をリポジトリの最上位に置きます。`github-pages`フォルダー自体を置くのではありません。
3. `Settings → Pages` を開きます。
4. `Build and deployment → Source` を `Deploy from a branch` にします。
5. `Branch` を `main`、フォルダーを `/(root)` にして保存します（使用ブランチが異なる場合はそのブランチを選択）。
6. 公開完了後、Pages設定画面に表示されるURLを開きます。

一般的なプロジェクトのURLは `https://ユーザー名.github.io/リポジトリ名/` です。
公式手順：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 第2セット以降を追加

1. 新しい5問を収録した単一HTMLを `n4-reading-02.html` として同じ階層に追加します。以降は `03`、`04`…と増やします。
2. 新しいセットにも `index.html` へ戻る相対リンクを付けます。
3. 一覧の `index.html` にある `SET START` から `SET END` のカードを複製し、リンク、セット番号、タイトル、内容を更新します。
4. 公開ブランチへ変更を保存すると、GitHub Pagesに反映されます。

既存の問題ファイル名は維持すれば、共有済みのリンクも引き続き使えます。
架空の未公開セットへのリンクは作らず、完成したセットだけ一覧に追加してください。

## 利用

各セットを直接ブラウザーで開いても練習できます。回答はサーバーへ送信されません。ページの再読み込みで回答はリセットされます。採点にはJavaScriptが必要です。

## 編集

問題データは各セットHTML内の `const questions` にまとまっています。`answer` は元の `choices` の位置を0から数えた値です。表示順をシャッフルしてもこの値は変更しません。`explanations` の並びは元の選択肢に合わせます。
