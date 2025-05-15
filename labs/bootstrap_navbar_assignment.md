
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

**以下のコードを、`<body>` タグの中（開始タグ `<body>` と終了タグ `</body>` の間）に貼り付けてください。**


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

---

## ステップ 4：自分のアプリにあわせてカスタマイズ


- `大学ポータル` → 自分のプロジェクト名やサービス名に変更  
- リンク名を自由に変更（例：サークル、図書館、マイページ、設定 など）

---

## ステップ 5：追加のデザイン・機能（任意）

### ダークテーマに変更（背景・テキストの組み合わせ）：

Bootstrapでは、ナビバーの背景色（`bg-*`）と文字色（`navbar-*`）の組み合わせで
デザインテーマを調整できます。

**よく使う組み合わせ例：**
- `navbar-dark bg-dark`（黒背景に白文字）
- `navbar-dark bg-primary`（青背景に白文字）
- `navbar-light bg-warning`（黄色背景に黒文字）
- `navbar-light bg-light`（白背景に黒文字）



```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
```

### ブランド名に色をつける（`text-*` クラス）：

`text-*` クラスを使うことで、文字にBootstrapのテーマカラーを適用できます。

**よく使う色の例：**
- `text-primary`（青）
- `text-success`（緑）
- `text-warning`（黄色）
- `text-danger`（赤）
- `text-info`（水色）
- `text-muted`（グレー）


```html
<a class="navbar-brand text-warning fw-bold" href="#">わたしのアプリ</a>
```


### ドロップダウンメニューを追加：

```html
<li class="nav-item dropdown">
  <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
    メニュー
  </a>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">プロフィール</a></li>
    <li><a class="dropdown-item" href="#">設定</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">ログアウト</a></li>
  </ul>
</li>
```


### 検索ボックスを追加（任意）：


```html
<form class="d-flex" role="search">
  <input class="form-control me-2" type="search" placeholder="検索" aria-label="検索">
  <button class="btn btn-outline-success" type="submit">検索</button>
</form>
```


---

## ステップ 6：動作確認
- ウィンドウを縮めて、メニューがハンバーガー形式に切り替わるか確認  
- 追加した項目が正しく動作するか確認

---

## 提出方法（Padlet）

1. 完成した `index.html` をブラウザで開いて表示  
2. スクリーンショットを撮る（Mac: Shift+Cmd+4 / Windows: Win+Shift+S）  
3. Padletに投稿（以下の内容）：
   - タイトル（アプリ名 or ナビバー名）  
   - スクリーンショット画像  
   - 説明（工夫した点、使った機能など）

---

## チャレンジ課題（上級者向け）

### Bootstrapコンポーネントを追加：
- **バナー（Alert）**

```html
<div class="alert alert-info text-center" role="alert">
  新しいアップデートが公開されました！
</div>
```

- **カード（Card）**

```html
<div class="card" style="width: 18rem;">
  <img src="https://via.placeholder.com/150" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">おすすめ記事</h5>
    <p class="card-text">この機能はユーザー体験を向上させます。</p>
    <a href="#" class="btn btn-primary">続きを読む</a>
  </div>
</div>
```

---

### GitHub Pagesで公開（アカウントを持っている人向け）

1. GitHubアカウントにログイン  
2. 新しいリポジトリを作成（例：`my-navbar-project`）  
3. `index.html` をアップロードまたはGitでプッシュ  
4. `Settings` → `Pages` → ブランチを `main` に設定し、ルート(`/`)を選択  
5. 発行されたURLをコピーしてPadletに貼る

例：`https://yourusername.github.io/my-navbar-project/`

