To start mysql, in the terminal, type in `mysql -u root`

# Create a new database user
In the MySQL CLI:
```
CREATE USER 'ahkow'@'localhost' IDENTIFIED BY 'rotiprata123';
```

```
GRANT ALL PRIVILEGES on sakila.* TO 'ahkow'@'localhost' WITH GRANT OPTION;
```
**Note:** Replace *sakila* with the name of the database you want the user to have access to
 
 ```
FLUSH PRIVILEGES;
```
create table book (
    book_id int unsigned auto_increment primary key,
    title varchar(200) not null,
    page_count int,
    ISBN varchar(200) default ''
) engine = innodb;

create table author (
    author_id int unsigned auto_increment primary key,
    first_name varchar(200) not null,
    last_name varchar(200) not null
) engine = innodb;

create table Publisher (
    publisher_id int unsigned auto_increment primary key,
    website varchar(200) not null,
    email varchar(200) not null
) engine = innodb;

create table review (
    review_id int unsigned auto_increment primary key,
    review text
) engine = innodb;

create table user (
    user_id int unsigned auto_increment primary key,
    dob datetime
) engine = innodb;


create table loan (
    loan_id int unsigned auto_increment primary key,
    due_date datetime,
    date_borrowed datetime
) engine = innodb;