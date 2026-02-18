# 模写プロジェクト：テンプレート

## 🚀 Git / GitHub コマンド備忘録
WindowsのVSCode上にて **Git Bash** を使用。

### 1. 初期設定（プロジェクト開始時）
1. GitHubでリポジトリを作成（URLをコピー）
2. `git init`
3. `git remote add origin [コピーしたURL]`
4. `git add .`
5. `git commit -m "first commit"`
6. `git branch -M main`
7. `git push -u origin main`

### 2. 日々の作業（呪文）
1. `git status` （現在の変更を確認）
2. `git pull` （念のため最新を読み込む）
3. `git add .`
4. `git commit -m "修正内容"`
5. `git push`

---

## 🏗️ コーディングルール：Sass(SCSS) + BEM

### 1. 開発フロー
- **編集ファイル**: `scss/style.scss`
- **出力ファイル**: `css/style.css`（自動生成されるため直接編集禁止）
- **コンパイル**: VSCodeのステータスバーにある **「Watch Sass」** を必ずONにする。

### 2. クラス名の付け方（BEM）
- **親子関係**: `__`（アンダースコア2つ）で繋ぐ。
- **状態（Modifier）**: `--`（ハイフン2つ）で繋ぐ。
- **Sassネスト**: `&__inner` のように `&`（アンパサンド）を活用する。

### 3. レスポンシブ管理
- 個別の `sp.css` は使用せず、`style.scss` 内で **`@include sp { ... }`** を使用して一括管理する。

---

## 📐 レイアウト構成案
- 状況によって変える
- **サイト最大幅**: `1000px`
- **共通パディング**: `16px`
- **メインビジュアル**: `全幅（width: 100%）`
- **ブレイクポイント**: `767px`（これ以下をスマホとする）

---

## 📂 フォルダ構造
root/
 ├─ index.html
 ├─ img/
 ├─ scss/
 │   └─ style.scss （★ここを編集）
 └─ css/
     ├─ style.css （自動生成）
     └─ style.css.map （デバッグ用）