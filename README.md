スキーマ管理
=================

## インストール
```sh
$ bundle install --path vendor/bundler
```

## DB設定
```
$ cp database.yml.origin database.yml
```

```database.yml

```

## 基本的な使い方
```sh
# 環境名
#    開発環境 → development
#    本番環境 → production
# コマンド
#    DBからスキーマファイルを出力 → export
#    スキーマファイルをDB適用のテスト → dry-run
#    スキーマファイルをDBに適用 → apply
$ bundle exec rake 環境名:コマンド[DB名]
```

## 使用例
### 開発環境のDBからスキーマファイルをExport
```sh
$ bundle exec rake development:export[xxx]
```

### 本番環境のDBにスキーマファイル適用のテスト
```sh
$ bundle exec rake production:dry-run[xxx]
```

### 本番環境のDBにスキーマファイルを適用
```sh
$ bundle exec rake production:apply[xxx]
```
