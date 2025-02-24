![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Answers

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.

**`Query`**: {name: {$eq: "Babelgum"}}
**`project`**: {name: 1, _id: 0}
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

**`Query`**: {number_of_employees: {$gt:5000}}
**`Project`**: n/a
**`Sort`**: {number_of_employees: 1} 
**`Skip`**: 0
**`Limit`**: 20

### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

**`Query`**: {founded_year: {$gte: 2000, $lte: 2005}}
**`Project`**: {name: 1, founded_year: 1, _id: 0}
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 4. All the companies that had a Valuation Amount of more than 100.000.000 and have been founded before 2010. Retrieve only the `name` and `ipo` fields.

**`Query`**: {'ipo.valuation_amount': {$gt: 100000000}, founded_year: {$lt: 2010}}
**`Project`**: {name: 1, ipo: 1, _id: 0}
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 5. All the companies that have less than 1000 employees and have been founded before 2005. Order them by the number of employees and limit the search to 10 companies.

**`Query`**: {number_of_employees: {$lt: 1000}, founded_year: {$lt: 2005}}
**`Project`**: n/a
**`Sort`**: {number_of_employees: 1}
**`Skip`**: 0
**`Limit`**: 10

### 6. All the companies that don't include the `partners` field.

**`Query`**: {partners: {$exists: false}}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 7. All the companies that have a null type of value on the `category_code` field.

**`Query`**: {category_code: {$type: 'null'}}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 8. All the companies that have at least 100 employees but less than 1000. Retrieve only the `name` and `number of employees` fields.

**`Query`**: {number_of_employees: {$gte: 100, $lt: 1000}}
**`Project`**: {name: 1, number_of_employees: 1, _id: 0}
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 9. Order all the companies by their IPO price in a descending order.

**`Query`**: n/a
**`Project`**: n/a
**`Sort`**: {'ipo.valuation_amount': -1}
**`Skip`**: 0
**`Limit`**: 0

### 10. Retrieve the 10 companies with most employees, order by the `number of employees`

**`Query`**: n/a
**`Project`**: n/a
**`Sort`**: {number_of_employees: -1} 
**`Skip`**: 0
**`Limit`**: 10

### 11. All the companies founded on the second semester of the year. Limit your search to 1000 companies.

**`Query`**: {founded_month: {$gte: 6}}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 1000

### 12. All the companies founded before 2000 that have an acquisition amount of more than 10.000.000

**`Query`**: {founded_year: {$gt: 2000}, 'acquisition.price_amount': {$gt: 10000000}}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 13. All the companies that have been acquired after 2010, order by the acquisition amount, and retrieve only their `name` and `acquisition` field.

**`Query`**: {'acquisition.acquired_year': {$gt: 2015}}
**`Project`**: {name: 1, acquisition: 1, _id: 0}
**`Sort`**: {'acquisition.price_amount': 1}
**`Skip`**: 0
**`Limit`**: 0

### 14. Order the companies by their `founded year`, retrieving only their `name` and `founded year`.

**`Query`**: n/a
**`Project`**: {founded_year: 1, name: 1, _id: 0}
**`Sort`**: {founded_year: 1}
**`Skip`**: 0
**`Limit`**: 0

### 15. All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their `acquisition price` in a descending order. Limit the search to 10 documents.

**`Query`**: {founded_day: {$lte: 7}}
**`Project`**: n/a
**`Sort`**: {'acquisition.price_amount': -1}
**`Skip`**: 0
**`Limit`**: 10

### 16. All the companies on the 'web' `category` that have more than 4000 employees. Sort them by the amount of employees in ascending order.

**`Query`**: {category_code: {$eq: 'web'}, number_of_employees: {$gt: 4000}}
**`Project`**: n/a
**`Sort`**: {number_of_employees: 1}
**`Skip`**: 0
**`Limit`**: 0

### 17. All the companies whose acquisition amount is more than 10.000.000, and currency is 'EUR'.

**`Query`**: {$and: [{'acquisition.price_amount': 10000000}, {'acquisition.price_currency_code': 'EUR'}]}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0

### 18. All the companies that have been acquired on the first trimester of the year. Limit the search to 10 companies, and retrieve only their `name` and `acquisition` fields.

**`Query`**: {'acquisition.acquired_month': {$lte: 4}}
**`Project`**: {name: 1, acquisition: 1, _id: 0}
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 10

### 19. All the companies that have been founded between 2000 and 2010, but have not been acquired before 2011.

**`Query`**: {founded_year: {$gte: 2000}}, {founded_year: {$lte: 2010}}, {'acquisition.acquired_year': {$gte: 2012}}
**`Project`**: n/a
**`Sort`**: n/a
**`Skip`**: 0
**`Limit`**: 0
