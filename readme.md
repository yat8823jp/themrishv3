# themrish v3

for WordPress theme develop auxiliary tool

WordPressのテーマ開発補助ツールです。

ブラウザシンクによるソースファイル保存時のページリロード sassコンパイラ ( dart-sass ) jsコンパイラ

## ディレクトリ構成
```
root
├─ public            # WordPress main body storage directory
|  ├─ wp-content
|  |  ├─ plugins
|  |  └─ themes
|  |     └─ themrish   # themrish theme directory
│  ├─ ...
|  └─ ...
├─ .git
├─ .gitignore
└─ README.md
```

## 必要な環境

- WordPress 5.9.0 以上
- [Local](https://local.getflywheel.com/) by Flywheel もしくはその他開発環境（PHP, MySQL）
- Node v12.13.1 以上

## 依存アプリケーション

- node.js version: v12.13.1 later
- npm version: 6.12.1 later
- gulp version: 4.0.2 later
- babel babel2015
- browsersync

## 使い方
### 1."[Local by Flywheel](https://local.getflywheel.com/)"によるWordPressのインストール

### 2.リポジトからデータをプル
``` git pull origin git@github.com:yat8823jp/themrishv3.git ```

### 3.クローンしたファイルの移動

``` themrish ``` ディレクトリに入っている

- .git
- .gitignore
- README.md

を ```public``` と同一階層に移動（ディレクトリ構成と同じにする）し、``` themrish ``` ディレクトリを削除

### 4.npm の実行

テーマ用ディレクトリに移動
``` cd public/wp-content/themes/themrish/ ```

``` npm install ```

### 5.gulpを起動して開発を開始

``` npx gulp ```

## sass

- [Dart Sass](https://www.npmjs.com/package/sass) を採用
- sass のインポートには @import ではなく @use 及び @forward を利用してください
- [gulp-sass-glob-use-forward](https://www.npmjs.com/package/gulp-sass-glob) を利用しているのでディレクトリ以下のファイルを読み込み可能
- スマホファーストを採用。mixin には tablet 600px~ と PC 1025px~ を採用

## スタイルガイド

- [Fractal ](https://www.npmjs.com/package/@frctl/fractal) を採用
- 定義ファイルは ` /src/styleguide/ ` に書いてください
- SASS で記述している ` component ` は ` src/styleguide/components/ ` 以下に自動でディレクトリを作成します
- ` gulp styleguide ` にてビルドとともにブラウザシンクが立ち上がります

## version

- 3.0.0 release