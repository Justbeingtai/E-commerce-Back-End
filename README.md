# E-commerce Back End

## Description

This project is a back end for an e-commerce website built with Sequelize and PostgreSQL. It allows for full CRUD operations on categories, products, and tags. The application follows RESTful API design principles, and the routes allow for seamless interaction with the database. 

- **Motivation**: The motivation for this project was to build a scalable back end for an e-commerce platform that can manage products, categories, and tags.
- **Why build this project?**: This project was built to demonstrate the development of a database-driven API using modern technologies like Express.js and Sequelize. 
- **Problem it solves**: This project allows online stores to manage their product catalog by creating, updating, deleting, and viewing products, tags, and categories.
- **What did I learn?**: I learned how to build a back end with Express.js, use Sequelize as an ORM, and work with PostgreSQL for database management.

## Table of Contents

- [Usage](#usage)
- [Credits](#credits)
- [License](#license)
- [Features](#features)
- [How to Contribute](#how-to-contribute)
- [Tests](#tests)
- [Installation](#installation)
  - Step 1: Clone the Repository
  - Step 2: Navigate to the Project Directory
  - Step 3: Install Dependencies
  - Step 4: Set Up the PostgreSQL Database
  - Step 5: Run Schema and Seed Commands
  - Step 6: Start the Server


## Usage

Once the server is running, you can interact with the API using a tool like [Insomnia](https://insomnia.rest/).

Here is an example of the homepage:

![Homepage Screenshot](/assets/images/VIDEOGIF.gif)\

Here is a link where you can Download the video: 
[Download Video](assets/images/video.mp4)


### Categories API

- **GET All Categories**: 
  - **Method**: `GET`
  - **URL**: `http://localhost:3001/api/categories`
  - **Response**: A list of categories with associated products.

- **GET Category by ID**: 
  - **Method**: `GET`
  - **URL**: `http://localhost:3001/api/categories/1`
  - **Response**: A single category with its associated products.

- **POST Create Category**: 
  - **Method**: `POST`
  - **URL**: `http://localhost:3001/api/categories`
  - **Body**:
    ```json
    {
      "category_name": "Accessories"
    }
    ```

- **PUT Update Category**:
  - **Method**: `PUT`
  - **URL**: `http://localhost:3001/api/categories/1`
  - **Body**:
    ```json
    {
      "category_name": "Updated Category"
    }
    ```

- **DELETE Category**:
  - **Method**: `DELETE`
  - **URL**: `http://localhost:3001/api/categories/1`

### Products API

- **POST Create Product**: 
  - **Method**: `POST`
  - **URL**: `http://localhost:3001/api/products`
  - **Body**:
    ```json
    {
      "product_name": "Running Shoes",
      "price": 99.99,
      "stock": 50,
      "category_id": 4,
      "tagIds": [1, 2]
    }
    ```

- **PUT Update Product**:
  - **Method**: `PUT`
  - **URL**: `http://localhost:3001/api/products/5`
  - **Body**:
    ```json
    {
      "product_name": "Updated Running Shoes",
      "price": 89.99,
      "stock": 60,
      "tagIds": [1, 3, 5]
    }
    ```

### Tags API

- **POST Create Tag**: 
  - **Method**: `POST`
  - **URL**: `http://localhost:3001/api/tags`
  - **Body**:
    ```json
    {
      "tag_name": "Summer"
    }
    ```

- **PUT Update Tag**:
  - **Method**: `PUT`
  - **URL**: `http://localhost:3001/api/tags/2`
  - **Body**:
    ```json
    {
      "tag_name": "Winter Collection"
    }
    ```

## Credits

Thanks to the Full-Stack Bootcamp team for providing the starter code and guiding the development process.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Features

- Full CRUD operations for categories, products, and tags.
- Sequelize ORM used for interacting with a PostgreSQL database.
- RESTful API routes for managing an e-commerce store.

## How to Contribute

If you would like to contribute to this project, please fork the repository, make your changes, and submit a pull request.

## Tests

There are no unit tests included in this project at this time. Future updates will include test coverage using Jest.



## Installation

Follow these steps to install and set up the project:

```md
1. Clone the repository:
   ```bash
   git clone <your-repository-url>
2. Navigate to the project directory:
    cd <project-directory>
3. Install dependencies:
    npm install
4. Set up the PostgreSQL database:
  Open PostgreSQL and create a new database
    CREATE DATABASE ecommerce_db;
  In the root of the project, create a .env file and add your PostgreSQL credentials:
    DB_NAME=ecommerce_db
    DB_USER=your_username
    DB_PASSWORD=your_password
5. Run the schema and seed commands to create the database structure and populate it with sample data:
    npm run seed
6. Start the server:
    npm start



