## Lab SQL Group By

```sql
-- 1

select last_name from sakila.actor
group by last_name
having count(*) = 1;
```


```sql
-- 2

select last_name from sakila.actor
group by last_name
having count(*) > 1;
```


```sql
-- 3

select staff_id, count(*) from sakila.rental
group by staff_id;
```


```sql
-- 4

select release_year, count(*) as num_films from sakila.film
group by release_year
order by release_year;
```


```sql
-- 5

select rating, count(*) as num_films from sakila.film
group by rating;
```

```sql
-- 6

select rating, round(avg(length),2) as avg_duration from sakila.film
group by rating
order by avg_duration desc;
```

```sql
-- 7

select rating, round(avg(length),2) as avg_duration from sakila.film
group by rating
having avg_duration > 120
order by avg_duration desc;
```

### By Iron Hack
