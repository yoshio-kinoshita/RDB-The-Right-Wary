# フラグの闇

## アンチパターンの解説

テーブルに削除という状態を持たせてしまう

## とりあえず削除フラグ

* クエリの複雑化
* UNIQUE制約が使えない
* カーディナリティが低い

## アンチパターンを生まないためには

* 事実のみを残す。 => 削除済みユーザは削除済みユーザテーブルに移動させる

### 状態を持たせるのは絶対にだめ

* 対象テーブルが小さく、INDEXが不要
* JOIN対象になることがない
* UNIQUE制約が不要

### 削除フラグを利用したくなるケース

* エンドユーザからみえなくしたいが、データは消したくない。
* 削除したデータを検索したい
* データを消さずにログに残したい
* 操作を謝ってもなかったことにしたい
* 削除してもすぐに元に戻したい

## アンチパターンのポイント

* とりあえず削除フラグ
* MySQLで論理削除と正しく付き合う方法
* PostgreSQLアンチパターン
