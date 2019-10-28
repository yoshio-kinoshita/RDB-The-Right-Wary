# やりすぎたJOIN

## アンチパターンの解説
* JOINに対する不理解
* 多段JOINと不要なJOIN
* JOINの内部表にINDEXがない
## JOINの特性
### JOINの種類
* INNER JOIN
* LEFT OUTER JOIN
* RIGTH OUTER JOIN
* FULL OUTER JOIN

### JOINの問題点
* JOINは掛け算
* JOINの回数が増えると急激に重くなる

### JOINのアルゴリズムの種類

* Nested Loop Join(NLJ)
* Hash Join
* Sort Merge Join

## アンチパターンを生まないためには

* JOINの特性を生かす

## アンチパターンのポイント

* JOINは必要最低限
* INDEXを適切に活用
* JOINするテーブルは小さくしてからJOINする
