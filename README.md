[![Build Status](https://travis-ci.org/KEINOS/Practice_Travis-CI.svg?branch=master)](https://travis-ci.org/KEINOS/Practice_Travis-CI)

## Travis CI's PHP Template with PHPUnit

とりあえず [Travis CI](https://ja.wikipedia.org/wiki/Travis_CI) で動く [PHPUnit](https://phpunit.de/manual/current/ja/) テスト付き「Hello World」の PHP テンプレート。

## 目標

1. 当リポジトリをコピーするだけで Travis CI のテストが通るテンプレートの作成。
2. 「Hello World」から徐々に実装できるようなシンプルなテンプレートであること。
3. クラスやメソッド中心でなく、関数（`functions`）のテストができるようなもの。

## 検証環境

以下の環境で動作した PHP スクリプトを、GitHub に Push した際に Travis CI の PHPUnit テストを通します。

- macOS High Sierra (OSX 10.13.4)
    - PHP 7.1.14 (cli)
- Raspbian Jessie (Debian GNU/Linux 8.0)
    - PHP 7.1.12 (cli)
- CentOS 7.4.1708 (Redhat Linux, Core) 
    - PHP 5.6.35 (cli) 
    - PHP 7.2.4 (cli)

- PHPUnit v.5.0.10 via Composer
    - PHP 5.6, 7.0, 7.1 コンパチは PHPUnit 5 であるため

## 構成

```
Practice_Travis-CI/
	┣━ README.md （このファイル）
	┣━ .git/ （このリポジトリの git 情報）
	┣━ .gitignore/ （git 同期で除外するファイル／ディレクトリを指定）
	┣━ .travis.yum （Travis CI の設定ファイル）
	┣━ composer.json （PHPUnit インストール用 Composer 設定ファイル）
	┣━ src/ （メインとなるソースコード）
	┃	┣━ index.php
	┃	┣━ Functions.php （ユーザ関数一覧）
	┃	┗━ Classes.php （クラス一覧）
	┗━ test/ （Travis CI で実行するテスト）
		┗━ FunctionsTest.php
```	
