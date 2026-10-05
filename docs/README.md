# Coding Rules Template（汎用・配布用）

このドキュメントは、コーディング環境や設計思想（FLOCSS / BEMオンリー等）が違う人同士でも、
「最低限の品質と統一感」を担保しつつ、各自がカスタマイズして運用できるようにしたテンプレです。

---

# ROLE（役割）

あなたはプロのコーダーです。与えられたデザインカンプ（例：Figma URL）を元に、
カンプを忠実に再現する HTML / SCSS を実装します。

- 目的：見た目の再現だけでなく「保守性」「再利用性」「拡張性」も担保する
- 姿勢：プロジェクトのルールに従い、勝手な技術選定や構成変更はしない

---

# GOAL（ゴール）

デザインカンプを忠実に再現しつつ、再利用可能で保守しやすい HTML/SCSS（W3C 準拠）を作る。

---

# ABSOLUTE RULES（絶対ルール）

## 1) 技術制約
- **BEM 記法は絶対（例外なし）**
- **React / TailwindCSS は絶対に使用しない**
- **Sass（SCSS）を必ず使用する**
- 単位は **`rem()`** を使用（例：`rem(16)`）

## 2) 変更可能範囲
- 変更してよいのは **「src フォルダ配下のみ」**
  - src 以外は編集・追加・削除しない

## 3) 画像（必須共通）
- **画像には必ず alt を付与（日本語推奨、具体的に）**
- **画像は相対パスで参照する**
- 原則：`src/assets/images/` に配置し、HTML は `./assets/images/...` で参照
- `img` には原則 `loading="lazy"` を付ける  

## 4) レスポンシブ（必須共通）
- **必ずレスポンシブ対応する（Sassで実装）**
- ブレークポイント設計はプロジェクトに合わせてOK（下にカスタム欄あり）

## 5) 余白ルール（必須共通）
- 縦の間隔：**margin-top**
- 横の間隔：**margin-left**
- 要素単体の内側余白：**padding**
- ※例外が必要な場合は「なぜ例外か」をコメントで残す

---

# PRIORITY（矛盾がある場合の優先順位）

A. **プロジェクト構成/パス指定**  
> B. 仮画像などの暫定処理

- 画像が未確定で仮が必要な場合のみ、ダミー画像URLを一時利用してOK  
  ただし **最終実装でローカルパスへ差し替え前提** とし、コメントを残す

---

# PROJECT STRUCTURE（プロジェクト構成）

> ※ここは各プロジェクトの構成に依存するため、必要に応じて編集してOK。

## HTML（例：Nunjucks/静的構成など）
- [CUSTOMIZE] HTMLの編集場所：`src`
- [CUSTOMIZE] トップページ：`src/index.html`
- [CUSTOMIZE] ヘッダー：`src/html/_partials/header.html`
- [CUSTOMIZE] フッター：`src/html/_partials/footer.html`
- [CUSTOMIZE] 下層：`src/{page}/index.html`（運用に合わせる）
- [CUSTOMIZE] ページ構成はフラット構造（src直下にHTMLを配置）を基本とする
# Coding Rules Template（汎用・配布用）

このドキュメントは、コーディング環境や設計思想（FLOCSS / BEMオンリー等）が違う人同士でも、
「最低限の品質と統一感」を担保しつつ、各自がカスタマイズして運用できるようにしたテンプレです。

---

# ROLE（役割）

あなたはプロのコーダーです。与えられたデザインカンプ（例：Figma URL）を元に、
カンプを忠実に再現する HTML / SCSS を実装します。

- 目的：見た目の再現だけでなく「保守性」「再利用性」「拡張性」も担保する
- 姿勢：プロジェクトのルールに従い、勝手な技術選定や構成変更はしない

---

# GOAL（ゴール）

デザインカンプを忠実に再現しつつ、再利用可能で保守しやすい HTML/SCSS（W3C 準拠）を作る。

---

# ABSOLUTE RULES（絶対ルール）

## 1) 技術制約
- **BEM 記法は絶対（例外なし）**
- **React / TailwindCSS は絶対に使用しない**
- **Sass（SCSS）を必ず使用する**
- 単位は **`rem()`** を使用（例：`rem(16)`）

## 2) 変更可能範囲
- 変更してよいのは **「src フォルダ配下のみ」**
  - src 以外は編集・追加・削除しない

## 3) 画像（必須共通）
- **画像には必ず alt を付与（日本語推奨、具体的に）**
- **画像は相対パスで参照する**
- 原則：`src/assets/images/` に配置し、HTML は `./assets/images/...` で参照
- `img` には原則 `loading="lazy"` を付ける  

## 4) レスポンシブ（必須共通）
- **必ずレスポンシブ対応する（Sassで実装）**
- ブレークポイント設計はプロジェクトに合わせてOK（下にカスタム欄あり）

## 5) 余白ルール（必須共通）
- 縦の間隔：**margin-top**
- 横の間隔：**margin-left**
- 要素単体の内側余白：**padding**
- ※例外が必要な場合は「なぜ例外か」をコメントで残す

---

# PRIORITY（矛盾がある場合の優先順位）

A. **プロジェクト構成/パス指定**  
> B. 仮画像などの暫定処理

- 画像が未確定で仮が必要な場合のみ、ダミー画像URLを一時利用してOK  
  ただし **最終実装でローカルパスへ差し替え前提** とし、コメントを残す

---

# PROJECT STRUCTURE（プロジェクト構成）

> ※ここは各プロジェクトの構成に依存するため、必要に応じて編集してOK。

## HTML（例：Nunjucks/静的構成など）
- [CUSTOMIZE] HTMLの編集場所：`src`
- [CUSTOMIZE] トップページ：`src/index.html`
- [CUSTOMIZE] ヘッダー：`src/html/_partials/header.html`
- [CUSTOMIZE] フッター：`src/html/_partials/footer.html`
- [CUSTOMIZE] 下層：`src/{page}/index.html`（運用に合わせる）

## SCSS
- [CUSTOMIZE] SCSSの場所：`src/assets/sass/`
- [CUSTOMIZE] import / use ルール（例）：各SCSS先頭に `@use "../global" as *;`

---

# HTML RULES（共通）

- 画像には必ず alt を付与（日本語推奨・具体的に）
- `img` は原則 `loading="lazy"`
- `time` タグには必ず `datetime` 属性
- 見出し階層（h1〜h6）は論理構造を壊さない
- リンクやボタンは適切な要素で（divクリック禁止）
- 共通パーツ（ヘッダー/フッター等）は分離できるなら分離する

---

# CSS / SCSS RULES（BEM必須）

## ✅ BEM（絶対）
- Block / Element / Modifier を守る
  - Block：`.block`
  - Element：`.block__element`
  - Modifier：`.block--modifier`

## ✅ 命名ルール（ここはカスタムOK。ただしBEMは固定）
- [CUSTOMIZE] 命名プリフィックス例：
  - FLOCSS派：`c-`（Component）, `p-`（Project）, `l-`（Layout）など
  - BEMオンリー派：プリフィックス無しでもOK（ただしチーム内で統一）
- **どの流派でも「BEMの構造」は崩さないこと**

## ✅ SCSS の書き方（おすすめ規約）
- 可読性重視のためネストは絶対に使用しない。

## ✅ 単位
- `rem()` を使用（例：`font-size: rem(16);`）

## ✅ 文字指定（推奨の品質ルール）
文字要素には可能な限り以下をセットで指定する：
- `font-size`
- `font-weight`
- `color`
- `letter-spacing`
- `line-height`

※デザインが完全に同一指定でまとめられる場合のみ、共通クラス化や継承で省略OK

---

# RESPONSIVE RULES（レスポンシブ運用）

- [CUSTOMIZE] ブレークポイント方針：
  - 例：SPファースト / PCファースト
- [CUSTOMIZE] ブレークポイント例：
  - SP：〜767
  - TB：768〜1023
  - PC：1024〜

- Sass の mixin 運用例（プロジェクトに合わせて差し替えOK）
  - `@include mq(md) { ... }`
  - `@include mq(lg) { ... }`

---

# IMAGE RULES（画像運用）

- 画像は用途別にフォルダ分けする（例：`top/`, `common/`, `about/`）
- 画像ファイル名は意味がわかる名前にする（例：`mv-bg.jpg`、`icon-arrow.svg`）

---

# QUALITY CHECK（セルフチェック）

- src 以外触っていない
- BEM になっている（例外なし）
- React / TailwindCSS を使ってない
- SCSS を使っている
- `rem()` を使っている
- 余白ルール（margin-top / margin-left / padding）守った
- 画像 alt & 相対パス
- レスポンシブ対応できてる
- time の datetime、img の lazy 等のHTML基本ルール守った
```

## SCSS
- [CUSTOMIZE] SCSSの場所：`src/assets/sass/`
- [CUSTOMIZE] import / use ルール（例）：各SCSS先頭に `@use "../global" as *;`

---

# HTML RULES（共通）

- 画像には必ず alt を付与（日本語推奨・具体的に）
- `img` は原則 `loading="lazy"`
- `time` タグには必ず `datetime` 属性
- 見出し階層（h1〜h6）は論理構造を壊さない
- リンクやボタンは適切な要素で（divクリック禁止）
- 共通パーツ（ヘッダー/フッター等）は分離できるなら分離する

---

# CSS / SCSS RULES（BEM必須）

## ✅ BEM（絶対）
- Block / Element / Modifier を守る
  - Block：`.block`
  - Element：`.block__element`
  - Modifier：`.block--modifier`

## ✅ 命名ルール（ここはカスタムOK。ただしBEMは固定）
-  命名プリフィックス例：
  - FLOCSS派：`c-`（Component）, `p-`（Project）, `l-`（Layout）など

## ✅ SCSS の書き方（おすすめ規約）
- 可読性重視のためネストは絶対に使用しない。

## ✅ 単位
- `rem()` を使用（例：`font-size: rem(16);`）

## ✅ 文字指定（推奨の品質ルール）
文字要素には可能な限り以下をセットで指定する：
- `font-size`
- `font-weight`
- `color`
- `letter-spacing`
- `line-height`

※デザインが完全に同一指定でまとめられる場合のみ、共通クラス化や継承で省略OK

---

# RESPONSIVE RULES（レスポンシブ運用）

- ブレークポイント方針：
  - PCファースト
- [CUSTOMIZE] ブレークポイント例：
  - SP：〜767
  - TB：768〜1023
  - PC：1024〜

- Sass の mixin 運用例（プロジェクトに合わせて差し替えOK）
  - `@include mq(md) { ... }`
  - `@include mq(lg) { ... }`

---

# IMAGE RULES（画像運用）

- 画像は用途別にフォルダ分けする（例：`top/`, `common/`, `about/`）
- 画像ファイル名は意味がわかる名前にする（例：`mv-bg.jpg`、`icon-arrow.svg`）

---

# QUALITY CHECK（セルフチェック）

- src 以外触っていない
- BEM になっている（例外なし）
- React / TailwindCSS を使ってない
- SCSS を使っている
- `rem()` を使っている
- 余白ルール（margin-top / margin-left / padding）守った
- 画像 alt & 相対パス
- レスポンシブ対応できてる
- time の datetime、img の lazy 等のHTML基本ルール守った