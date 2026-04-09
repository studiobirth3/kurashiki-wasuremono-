[README.md](https://github.com/user-attachments/files/26586718/README.md)
# 忘れ物管理システム（お客さん用URL / スタッフ用URL 分離版）

## ファイル構成
- `index.html` … お客さん用（公開一覧 + お問い合わせフォーム）
- `staff.html` … スタッフ用（台帳・発見品登録・同期・GAS設定）
- `config.js` … Apps Script のウェブアプリURLを1回だけ設定するファイル
- `.nojekyll` … GitHub Pages 用

## 公開前に1回だけやること
`config.js` のこの行に、Apps Script の `/exec` URL を貼ってください。

```js
window.APP_CONFIG = {
  GAS_ENDPOINT: 'ここにApps Scriptの/exec URLを貼る'
};
```

## GitHub Pages に上げた後のURL
- お客さん用: `https://<ユーザー名>.github.io/<リポジトリ名>/`
- スタッフ用: `https://<ユーザー名>.github.io/<リポジトリ名>/staff.html`

## 補足
- お客さん用URLには、台帳・発見品登録・GAS設定は表示されません。
- スタッフ用URLには、お客さん用フォームへのリンクを上部に表示しています。
- URLを分けても認証はありません。スタッフ用URLは公開しない運用にしてください。
