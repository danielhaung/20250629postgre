## 建立資料表的語法

```sql
CREATE TABLE [IF NOT EXISTS] table_name (
   column1 datatype(length) column_constraint,
   column2 datatype(length) column_constraint,
   ...
   table_constraints
);
```

## 建立一個student的資料表

```sql
CREATE TABLE IF NOT EXISTS student(
   student_id SERIAL PRIMARY  KEY,
   name VARCHAR(20) NOT NULL,
   major VARCHAR(20) UNIQUE
);
```

## 刪除資料表

```sql
DROP TABLE IF EXISTS student;
```


## 新增1筆資料

```sql
INSERT INTO student (name, major)
VALUES ('呂育君','歷史');
```


## 新增多筆資料

```sql
INSERT INTO student (name, major)
VALUES ('小柱','生物'),('信忠','英文');
```


## 取得資料

```sql
SELECT
select_list
FROM
table_name
WHERE

```


```sql
SELECT
student_id ,name,major
from student;

select name,major
from student;
```

```sql
select *
from student
where name='信忠';
```

```sql
select *
from student
ORDER BY  student_id ASC;
```

```sql
select *
from student
ORDER BY  student_id DESC
LIMIT 3;
```

## 修改與刪除

```sql
UPDATE student 
SET name='阿柱',
	major= '數學'
WHERE student_id = 2;
```


```sql
DELETE FROM student 
WHERE student_id = 2;
```


```sql
DELETE FROM student 
WHERE student_id in (1,3,4);
```
