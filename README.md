# 余景 YOKEI — Lumi Design 制作実績

架空の設計事務所を題材としたデモサイトです。実在の設計・施工・資格・顧客実績を示すものではありません。既存のLumi DesignやBIG WANのファイルは変更していません。

## ブランド・サイト設計
「暮らしに、余白の景色を。」光、庭、時を重ねる自然素材を軸に、余白と生活の風景を設計するブランド。和文の明朝と小さな欧文、温白色・墨色・鈍い朱色、誌面を意識した非対称のレイアウトです。ロゴは和文タイポグラフィと独自に組んだ欧文表記。

トップ → 施工事例（カテゴリー絞り込み）→ 3つの事例詳細（拡大ギャラリー）→ 私たちについて → 家づくりの流れ・FAQ → 相談入力・確認画面。個人情報案内、404、送信結果案内もあります。

## ファイル
- `dist/`: 完成済み静的サイト。編集・配信の本体。ビルド不要。
- `dist/assets/style.css`: レスポンシブデザイン
- `dist/assets/app.js`: メニュー、スクロール表示、絞り込み、ギャラリー、デモフォーム
- `netlify.toml`: 公開フォルダーとセキュリティヘッダー
- `ASSETS.md`: 画像・素材と利用条件
- `TESTS.md`: 実行した検査と未確認事項
- `PUBLISH.md`: 公開前チェックリスト
- `.openai/hosting.json`: Sitesプレビュー用。Netlifyでは参照されません。

## ローカル確認
Python 3があればプロジェクト直下で `python3 -m http.server 8000 --directory dist` を実行し、`http://localhost:8000` を開いてください。トップのHTMLを直接開くfile方式は、ルート相対URLのため対応しません。

## GitHubとNetlify
1. GitHubで新しい空のリポジトリを作成。既存プロジェクトを流用しないでください。
2. このフォルダーのファイルをアップロード。隠しファイル以外でもNetlify公開可能です。
3. NetlifyのImport an existing projectでリポジトリを選択。
4. Build commandは空欄、Publish directoryは `dist`。設定はnetlify.tomlが優先されます。
5. デプロイしてリンク、404、ヘッダーを確認。
6. 独自ドメインを設定したら、全HTMLのcanonical・og:url・og:imageとsitemap.xml・robots.txtのドメインを置換。

NetlifyアカウントとGitHubの接続・権限は確認していません。GitHubへの保存やNetlifyへの公開は行っていません。

## フォーム
現在はデモ専用です。ブラウザの必須・メール形式・文字数・過去日チェック、追加の空白チェック、確認画面までが動きます。送信はpreventDefaultで必ず停止します。通信・保存・成功の表示はしません。テスト情報だけを入力してください。JavaScriptが無効の場合は確認ボタンを無効にしています。

Netlify Forms用のフォーム名、hidden form-name、data-netlify、honeypotは準備済みです。実運用する場合はPUBLISH.mdに従い、デモのまま送信ボタンだけを有効にしないでください。

## 管理
ページの文章は各index.htmlから編集できます。画像は1536px版と720px版を同名で差し替え。全ページの共通ヘッダー・フッターを変更するときは全HTMLに反映してください。外部ライブラリ、CDN、解析ツール、外部フォントへの依存はありません。
