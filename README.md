# patika.dev-SQL-Practice07
patika.dev-SQL-Practice07

🔸film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
``` sql
SELECT RATING,
	COUNT(RATING)
FROM FILM
GROUP BY RATING

```
🔸film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
``` sql
SELECT replacement_cost, COUNT(*)
FROM FILM
GROUP BY replacement_cost
HAVING COUNT(*)>50
ORDER BY replacement_cost

```
🔸 customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 

``` sql
SELECT STORE_ID,
	COUNT(*)
FROM CUSTOMER
GROUP BY STORE_ID
```
🔸city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
✅Country Id :44
        Count:60
 ```sql
SELECT COUNTRY_ID,
	COUNT(*)
FROM CITY
GROUP BY COUNTRY_ID
ORDER BY COUNT(CITY) DESC
LIMIT 1
```
app.patika.dev/emintunahan
