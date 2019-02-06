# Building and mining Knowledge Graphs
## Assignment 1
### Datasets
#### GeoNames
Contains geographical information about countries. The header of the file are:

- **ISO**
- **ISO3**
- **ISO-Numeric**
- **fips**
- **Country**
- **Capital**
- **Area**
- **Population**
- **Continent**
- **tld**: top level domain. Eg: '.uk'.
- **CurrencyCode**
- **CurrencyName**
- **Phone**
- **Postal Code Format**
- **Postal Code Regex**
- **Languages**
- **geonameid**
- **neighbours**: Neighbours countries in ISO format.
- **EquivalentFipsCode**

#### WorldBank
Contains the GDP from 1960 to 2017 for 276 countries. A sample of the data is:

```xml
<record>
    <country key="LBN">Lebanon</country>
    <field name="Item" key="NY.GDP.MKTP.CD">GDP (current US$)</field>
    <year>2017</year>
    <value>53576985686.6998</value>
</record>
```

### Queries
The queries are:
1. List all countries with population less than 50.000 and order them from the smallest to the largest in terms of landmass area (square kilometres).
2. List the countries with the top 10 highest GDP values in 2017.
3. List the countries with the top 10 highest ​increases​ in GDP between 1960 and 2017.
4. Bonus query 1:​ For each continent, count the number of countries in that continent that are in the top 20 for highest ​increases​ in GDP between 1960 and 2017. Your answer should contain 2 values: the continent and the number of countries from the top 20 that are located in those continents (For example, Asia- 15, Europe - 5).
5. Bonus query 2:​ Construct the triples representing the GDP per capita for each country in 2017.
  - Directly insert the triples representing the GDP per capita for each country in 2017, into your triplestore on GraphDB.

### Requirements for the queries
Looks like the ISO3 key for the GeoNames.csv is the same than the key for the countries of the GDP.

1. Country name, population and area.
2. Country name and GDP 2017.
3. Country name and GDP 2017 and 1960.
4. Continent and GDP 2017 and 1960.
5. Country name and GDP 2017.