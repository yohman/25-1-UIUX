
# Bootstrapナビバー作成：授業内ステップバイステップ課題

## 課題の目的  
Bootstrapを使って、自分のアプリ・ウェブサイトに合ったナビバーを作成します。

## 実施時間  
約30〜40分（授業内課題）

---

## ステップ 1：プロジェクトの準備
1. VS Codeを開く  
2. 新しいフォルダを作成（例：navbar-workshop）  
3. フォルダの中に `index.html` ファイルを作成

---

## ステップ 2：基本HTMLテンプレートを貼り付け

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>学生ポータル</title>
  <!-- Bootstrap CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

</body>
</html>
```

---

## ステップ 3：Bootstrapナビバーを追加

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand fw-bold" href="#">大学ポータル</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
      aria-controls="navbarNav" aria-expanded="false" aria-label="ナビゲーションの切り替え">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">時間割</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">課題</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">学食メニュー</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">お知らせ</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

ブラウザで開いて、正しく表示されるか確認しましょう。

---

## ステップ 4：自分のアプリにあわせてカスタマイズ
- `大学ポータル` → 自分のプロジェクト名やサービス名に変更  
- 各リンクを、自分が作っているアプリに関係する項目に書き換える  
  - 例：サークル・図書館・マイページ・設定 など

---

## ステップ 5：色とスタイルの変更（自由課題）
以下のようにクラスを変更して、見た目を調整してみましょう：

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
```

```html
<a class="navbar-brand text-warning fw-bold" href="#">アプリ名</a>
```

---

## ステップ 6：動作確認（レスポンシブ対応）
- ウィンドウを縮めて、メニューが自動的にハンバーガーに切り替わるか確認  
- モバイル画面でも動作することを確認

---

## 提出方法（Padlet）
1. 完成した `index.html` をブラウザで表示  
2. スクリーンショットを撮る（Mac: Shift+Cmd+4 / Windows: Win+Shift+S）  
3. Padletに以下の内容で投稿：
   - タイトル：自分のアプリ名やナビバー名  
   - スクリーンショット画像  
   - 簡単な説明（リンク内容や工夫したポイント）

---

## チャレンジ課題（時間があれば）
- ナビバーに検索ボックスを追加してみる  
- ドロップダウンメニューを追加してみる  
- 自作CSSでデザインをカスタマイズしてみる
