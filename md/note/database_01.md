# データベースの基本概念

## 【データベースの設計概略】
データベース設計とは、格納するデータを分析して、効率よいテーブルを作成することである。効率よいテーブルを作成するために正規化を行う。

- 非正規形→
  - 第1正規化→第1正規形
  - 第2正規化→第2正規形
  - 第3正規化→第3正規形（完成）


* 第１正規化は、繰り返し項目部分を別テーブルとすること。  
  主キー（プライマリキー）…1行（1件分）を特定できる項目。  
  外部キー…関連したテーブル間を結ぶために設定する列のことで、データの整合性をデータベースに保証させるために利用する。  

* 第２正規化は、完全従属している項目と、部分従属している項目部分とを見つけ、部分従属している項目部分を別テーブルとし、リレーションを結ぶ。（テストに出るよ！）  
  完全従属…主キーにより決定する項目の関係。  
  部分従属…主キー項目の一部により決定する項目の関係。  

* 第３正規化は推移従属している項目を見つけて別テーブルとし、リレーションを結ぶ。  
  推移従属…主キー以外の項目により決定する項目。


## 【データベースの基本概念】
表形式のリレーショナルデータベース管理システム＝ RDBMS（Relational DataBase Management System）。  
RDBMSにはMySQLのほか、PostgreSQL、SQL Server、Oracle、Accessなど、さまざまなものがある。

### データベースの構造
MySQL（データベースエンジン）  
  ↳ データベース  
    ↳ テーブル  
      ↳ フィールド（列・カラム） → インデックス  
        ↳ レコード（行）  

* データベースエンジン  
  ツリー構造のもっとも上位にあるのがデータベースエンジン。MySQLがこれに相当する。  
* データベース  
  データベースはデータベースエンジンが管理している、その下位にあるデータの集合体のこと。  
* テーブル  
  1つのデータベースには、1つ以上のテーブルがある。  
* フィールド  
  表構造になっているテーブルにおいて、フィールドは表を構成する各列のこと。「カラム」または単に「列」と呼ばれることもある。  
* レコード  
  フィールドが表の列であるのに対して、レコードは表の各行のこと。「タプル」あるいは単に「行」と呼ばれることもある。  
  1つのレコードが1件のデータを表す。  
* インデックス  
  インデックスはレコードの索引となるもので、フィールドの1つの属性として付加することができる。必須ではないが、設定していないと検索の際に処理速度が遅くなる。また、主キーはそれだけでインデックス。  


メモ：SQLは言語。