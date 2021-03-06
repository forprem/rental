## Car Rental
[![Build Status](https://travis-ci.org/twistezo/car-rental.svg?branch=master)](https://travis-ci.org/twistezo/car-rental)

### Description
Web service for car rental company (non-commercial)

### Tools
Java, Spring, Hibernate, MySQL, Thymeleaf, Bootstrap, JavaScript, Travis CI

### Features
- various ways of search (e.g. by car, by calendar)
- order flow based on three pages and resume page:
1. check date range
2. fill customer data 
3. make payment 
4. get resume
- validation every order flow page's forms
- mail sender (with order resume)
- cancel button on every page cleans current session
- when everything is fine all data is saved to MySQL DB

### Requirements
Java, mySQL, Maven

### Run, test
```
Prepare new user and empty DB:
mysql -u root -p -e 'CREATE DATABASE IF NOT EXISTS car_rental;'
mysql -u root -p -e "CREATE USER 'dev'@'localhost' IDENTIFIED BY 'dev';"
mysql -u root -p -e "GRANT ALL ON car_rental.* TO 'dev'@'localhost';"

mvn spring-boot:run -> localhost:8080
mvn test
```

### Screenshots

<table>
    <tr>
        <td>
            <img src="http://i.imgur.com/8tyBBlU.png" width="500">
        </td>
        <td>
            <img src="http://i.imgur.com/eCGDN4m.png" width="500">
        </td>
    </tr>
</table>

### FIXME
After a few months email sender stop working. Probably by blocking the mail address through the provider.
