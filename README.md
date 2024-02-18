# E-commerce-app (backend)

This is a functional backend API for an e-commerce app. This API is built using Node.js and Sequelize.

## Table of Contents

- [Demo](#demo)
- [Usage](#usage)
- [Database Information](#database-information)
  - [Category](#category)
  - [Product](#product)
  - [Tag](#tag)
  - [ProductTag](#producttag)
- [Associations](#associations)
- [API Routes](#api-routes)
- [Technologies](#technologies)
- [Installation](#installation)

## Demo
A video walkthrough of this API's functionality

- 

## Usage

```terminal
npm start
````

This will run the server on `http://localhost:3001`

## Database information

### Category

- id (Integer, Primary Key)
- category_name (String)

### Product

- id (Integer, Primary Key)
- product_name (String)
- price (Decimal)
- stock (Integer, Default: 10)
- category_id (Integer, Foreign Key referencing Category)

### Tag

- id (Integer, Primary Key)
- tag_name (String)

### ProductTag

- id (Integer, Primary Key)
- product_id (Integer, Foreign Key referencing Product)
- tag_id (Integer, Foreign Key referencing Tag)

## Associations

- Product belongs to Category
- Category has many Product models
- Product belongs to many Tag models through ProductTag
- Tag belongs to many Product models through ProductTag

## API Routes

- `/api/products`: Product CRUD operations
- `/api/categories`: Category CRUD operations
- `/api/tags`: Tag CRUD operations
- `/api/product-tags`: ProductTag operations

## Technologies

Project is created with

Project is created with:  

- Javascript
- Node.js
- Sequelize
- MySQL2
- Express

## Installation

```terminal
npm init --y
```

```terminal
npm install express sequelize mysql2
```

Open up MySQL shell and input

```terminal
source db/schema.sql
```

and

```terminal
use ecommerce_db
```

In other terminal

```terminal
npm run seed
```

to start running application simply input

```terminal
npm run start
```
You can now test the routes in insomnia core on port 3001