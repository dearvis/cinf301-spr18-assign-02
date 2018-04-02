# cinf301-spr18-assign-02

(1.)
docker pull mysql

docker pull ubuntu

docker run --name sql -e MYSQL_ROOT_PASSWORD=one-p -e MYSQL_DATABASE=test -p 3306:3306 -d mysql

docker logs sql

docker run --name ubuntu --link sql:mysql -d mysql

sudo apt-get update

sudo apt-get install net-tools

docker exec -it d646ac629f79 /sbin/ifconfig eth0

mysql -u root -p -h 3306





(3.)
create database cars;

CREATE USER 'guest' @'192.168.99.100' IDENTIFIED BY 'one-p';

GRANT ALL PRIVILEGES ON * . * TO 'guest'@'192.168.99.100';

CREATE TABLE car_stats (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
make VARCHAR(20) NOT NULL,
model VARCHAR(20) NOT NULL,
year INT(5) NOT NULL,
color VARCHAR(10) NOT NULL,
engine VARCHAR(25) NOT NULL,
transmission VARCHAR(12) NOT NULL,
);		


INSERT INTO car_stats (make, model,year,color,engine,transmission)
VALUES
    ('Lamborgini', 'Gallardo', 2015, 'Yellow', 'six-cylinder','Automatic'),
    ('Ferrari', 'Italia', 2016, 'Gray', 'five-cylinder','Automatic'),
    ('Ford', 'Focus', 2014, 'Gray', 'four-cylinder','Automatic'),
    ('Porsche', 'Carrera GT', 2017, 'White', 'six-cylinder','Manual'),
    ('Nissan', 'Altima', 2015, 'Gray', 'three-cylinder','Automatic'),
    ('Cadillac', 'Escalade', 2016, 'Black', 'Five-cylinder','Automatic'),
    ('BMW', 'X2', 2018, 'Blue', 'seven-cylinder','Automatic');

Select * from car_stats;
