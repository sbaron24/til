## creating a table

```
CREATE TABLE cities {
	name VARCHAR(50),
 	country VARCHAR(50),
 	population INTEGER,
 	area INTEGER
};
```

## inserting values into a table

```
INSERT INTO cities (name, country, population, area)
VALUES
	('Delhi', 'India', 2812500, 2240),
  	('Shanghai', 'China', 22125000, 4015),
  	('Sao Paulo', 'Brazil', 20935000, 3043);
```

## getting values from a table

`SELECT * FROM cities;` selects all columns and rows\
`SELECT name, country FROM cities;` selects specified columns
