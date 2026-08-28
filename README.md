# World Database Java Application

A Java application that connects to the MySQL **World** database and provides database operations for countries, cities, and languages.

## Technologies

* Java
* JDBC
* MySQL
* DAO Pattern

## Features

### Countries

* Retrieve all countries
* Find a country by country code
* Find a country by name
* Find a country by region
* Insert a country
* Update country information
* Delete a country

### Cities

* Retrieve all cities
* Find cities by country
* Find cities by name
* Find a city by ID
* Find cities with a population over one million
* Insert a city
* Update city information
* Delete a city

### Languages

* Retrieve language information from the database

## Project Structure

```text
src/
├── App.java
├── daos/
│   ├── CityDao.java
│   ├── CountryDao.java
│   ├── Dao.java
│   ├── Database.java
│   └── LanguageDao.java
└── entities/
    ├── City.java
    ├── Country.java
    └── Language.java
```

The DAO classes handle database operations while the entity classes represent the data returned from the database.

## Database

The application uses the MySQL **World** sample database.

The database connection is handled through the `Database` class.

## Example Operations

The application demonstrates database operations such as:

```java
Country country = countryDao.findById("AGO");
```

```java
List<City> cities = cityDao.findByPopOverMillion();
```

```java
List<City> cities = cityDao.findByCountry("USA");
```

These operations demonstrate querying relational data through JDBC and mapping database records to Java objects.

## Purpose

This project demonstrates practical experience with Java database programming, JDBC, SQL queries, DAO architecture, object mapping, and CRUD operations.
