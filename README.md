# SQL_ODEV11
**Patika SQL eğitimi kapsamında yaptığım ödev 11**
--------------
1._actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım._
```sql
(SELECT  first_name FROM customer)
UNION
(SELECT first_name FROM actor);
```
2._actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım._
```sql
(SELECT  first_name FROM customer)
INTERSECT
(SELECT first_name FROM actor);
```
3._actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım._
```sql
(SELECT  first_name FROM customer)
EXCEPT
(SELECT first_name FROM actor);
```
4._İlk 3 sorguyu tekrar eden veriler için de yapalım._
```sql
(SELECT  first_name FROM customer)
UNION ALL
(SELECT first_name FROM actor);
-------------------------------
(SELECT  first_name FROM customer)
INTERSECT ALL
(SELECT first_name FROM actor);
-------------------------------
(SELECT  first_name FROM customer)
EXCEPT ALL
(SELECT first_name FROM actor);
```

---------------
**Sorgu senaryolarını [dvdrental.tar](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip) isimli dosyayı indirerek gerçekleştirebilirsiniz.**
