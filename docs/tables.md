# テーブル定義

## 書籍情報テーブル

書籍の情報を管理するテーブル

| 論理名 | 物理名 |データ型 | PKEY | NOT NULL| 備考 |
|:-:|:-:|:-:|:-:|:-:|:-:|
|書籍ID| BOOKID |INTEGER |○ |○ | AUTO_INCREMENT |
|タイトル| TITLE | VARCHAR(100) ○ | |
|著者| WRITER |VARCHAR(50)| ○ | |
|出版社ID | PUBLISHER | INTEGER| ○ | |
|価格 |PRICE |INTEGER  | |
|購入日| BOUGHT | DATE  | |
|書籍管理部署ID| MNGDEPT | INTEGER |○| |
|更新日| UPDATED |TIMESTAMP |○ | |
|更新者ID| UPDATOR | VARCHAR(20)| ○ | |

## ユーザマスタ

書籍の操作を行うユーザのマスタテーブル

| 論理名 | 物理名 |データ型 | PKEY | NOT NULL| 備考 |
|:-:|:-:|:-:|:-:|:-:|:-:|
|書籍ID| BOOKID |INTEGER |○ |○ | AUTO_INCREMENT |
|ユーザID| USERID| VARCHAR(100) ○ | |
|パスワード| PASSWORD |VARCHAR(50)| ○ | |
|所属部署ID| DEPTID | INTEGER | ○ | |
|名前| NAME |VARCHAR(50)| ○ | |

## 部署マスタ

ユーザが所属する部署を管理するマスタテーブル

| 論理名 | 物理名 |データ型 | PKEY | NOT NULL| 備考 |
|:-:|:-:|:-:|:-:|:-:|:-:|
|部署ID| ID |INTEGER |○ |○ | |
|名称| NAME| VARCHAR(100) ○ | |

## 出版社マスタ

出版社情報を管理するマスタテーブル

| 論理名 | 物理名 |データ型 | PKEY | NOT NULL| 備考 |
|:-:|:-:|:-:|:-:|:-:|:-:|
|出版社ID| ID |INTEGER |○ |○ | |
|名称| NAME| VARCHAR(100) ○ | |