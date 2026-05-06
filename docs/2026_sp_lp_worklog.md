# 2026_sp LP制作作業記録

作成日: 2026-05-07

## 対象ページ

- 公開URL: https://ouchi-english.jp/2026_sp/index.html
- 実装ファイル: `2026_sp/index.html`
- 使用画像:
  - `2026_sp/assets/hero-watercolor.jpg`
  - `2026_sp/assets/instructor-chiho.jpg`

## 制作内容

- `/001_course/index.html` の世界観をベースに、淡いピンク系のトーンで `/2026_sp/index.html` を作成。
- ヒーローイラストは既存の親子水彩イラストを流用。
- 内容は「AIと英語絵本を取り入れた、おうち英語2026スペシャルプログラム」として構成。
- サポート内容として、毎月1回60分の個人指導セッションと、毎月1回60分のグループコンサルを追加。
- 講師紹介にはプロフィール写真と紹介文を掲載。
- 「IT業界30年」の表記は使わず、「証券業界35年」に統一。

## 改行修正

ユーザー確認後、スマホ表示で見出しが不自然に折れていたため修正。

特に以下を調整:

- `こんな悩み、ありませんか。`
  - `こんな悩み、`
  - `ありませんか。`
  の2行になるよう固定。
- 長い見出しを意味のまとまりごとに `span.title-line` で分割。
- FAQの長い質問文は `span.phrase` で文節単位に分け、単語の途中で改行されにくいように調整。
- CSSに `word-break: keep-all;`、`line-break: strict;`、`overflow-wrap: normal;` を追加。
- モバイル表示でも `.nowrap` が解除されないように変更。

## 今後のLP制作ルールとして追加したこと

`mana-sales-letter` skillに、LP・サイト実装時の改行チェックルールを追加。

追加した主なルール:

- 日本語の単語・文節の途中で改行しない。
- 短い見出しは意味のまとまりで改行する。
- 長い見出しはブラウザ任せにせず、自然な改行位置を指定する。
- FAQ、ボタン、価格表示もスマホ幅で確認する。
- 1文字だけ次の行に落ちる、文末だけ孤立する、単語の途中で割れる箇所を公開前に確認する。

## Git履歴

- `ff99bcd Add 2026 special program page`
  - `/2026_sp/index.html` と画像アセットを追加。
- `cff4a3d Fix 2026 special page line breaks`
  - 見出し・FAQの不自然な改行を修正。

## 確認済み事項

- ローカル確認: `http://localhost:8081/2026_sp/index.html` で `200 OK`
- 公開確認: `https://ouchi-english.jp/2026_sp/index.html` で `200 OK`
- GitHub Pagesで新しいHTMLが返っていることを確認済み。
