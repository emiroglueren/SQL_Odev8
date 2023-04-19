# ODEV 8

Merhabalar,

    test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
    Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
    Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
    Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

Kolay Gelsin.

# CEVAPLAR

## Tablo oluşturma:

CREATE TABLE employee (
	id INTEGER NOT NULL,
	first_name VARCHAR(50) NOT NULL,
	birthday DATE NOT NULL,
	email VARCHAR(100) NOT NULL
);

## Veri ekleme:

insert into employee (id, first_name, email, birthday) values (1, 'Hilary', 'hlenthall0@bbc.co.uk', '17/10/1979');

...

insert into employee (id, first_name, email, birthday) values (50, 'Lutero', 'lpinar1d@census.gov', '20/2/1935');

## Sütunlara göre diğer sütunları güncelleme:

UPDATE employee
SET first_name = 'Eren', email = 'emirogleren@gmail.com', birthday = '23/02/1998'
WHERE id = 1;

UPDATE employee
SET id = 95, email = 'ödev8@gmail.com', birthday = '11/11/2000'
WHERE first_name = 'Laurene';

UPDATE employee
SET id= 101, first_name='ODEV 8', birthday = '01/01/2023'
WHERE email='dhonig16@wailey.com';

UPDATE employee
SET id=202, first_name = 'ODEV 8-1', email= 'deneme@gmail.com'
WHERE birthday = '20/2/1935';

UPDATE employee
SET first_name= 'Emiroglu',email='test@gmail.com', birthday ='05/05/1999'
WHERE id=2;

## Sütunlara göre satır silme işlemi:

DELETE FROM employee
WHERE id = 17;

DELETE FROM employee
WHERE id < 3;

DELETE FROM employee
WHERE first_name = 'Eren';

DELETE FROM employee
WHERE email='hdasper12@gravatar.com';

DELETE FROM employee
WHERE birthday = '2022-01-23';