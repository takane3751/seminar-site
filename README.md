# セミナー会員サイト 仕様コンフィギュレーター

石原先生のセミナー動画 会員サイトについて、構成（案内・申込・決済・拡散防止・閲覧期限・維持費方針）をトグルで切り替えると、構成モード・必要なもの・要件充足・概算費用が連動して表示される単一HTMLツールです。

## 特徴

- 外部依存なしの単一 `index.html`（CDN・ライブラリ不使用）。そのまま開けば動作します。
- KOEMO / ササキのシステムと同様、GitHub にブラウザから設置 → GitHub Pages で公開できます。

## GitHub Pages での公開手順（ブラウザのみ）

1. GitHub で新規リポジトリを作成（例: `seminar-site-spec`）。Public を選択。
2. 「uploading an existing file」から `index.html` をドラッグ&ドロップしてコミット。
3. リポジトリの Settings → Pages を開く。
4. Build and deployment の Source を「Deploy from a branch」にし、Branch を `main` / `(root)` に設定して Save。
5. 数十秒後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

## 編集

`index.html` の `<script>` 内、冒頭の `TOGGLES` と `computeReqs()` / `computeStack()` / `computeCost()` を編集すると、質問項目・要件・構成・費用ロジックを調整できます。

## 前提

- 会員登録は無料、受講で課金。会員ランク（有料/無料の階層）は持たない。
- 費用は2026年6月時点の概算・税別。為替やサービス改定で変動します。
