## Product Management API

## Project Title
  product management API
  
## Project Description
This project implements a CRUD (Create, Read, Update, Delete) API for managing products. It is built using Node.js, Express, and MongoDB, providing endpoints to perform operations such as creating a new product, retrieving product details, updating product information, and deleting products.
## Table of Contents
1. [Project Title](#project-title)
2. [Project Description](#project-description)
3. [Table of Contents](#table-of-contents)
4. [Prerequisites](#Prerequisites)
5. [How to Install and Run the Project](#how-to-install-and-run-the-project)
6. [How to Use the Project](#how-to-use-the-project)
7. [API Documentation](#api-documentation)
8. [Contributing](#contributing)

## Prerequisites
Before running this project locally, ensure you have the following installed:

* Node.js
* MongoDB
* npm (Node Package Manager)
## Installation
**Clone the repository:**
git clone https://github.com/yourusername/CRUD--API.git
cd CRUD--API
## Install dependencies:
npm install
## Set up environment variables:

Create a .env file in the root directory with the following variables:<br>
MONGO_URI=your_mongodb_connection_string<br>
Replace your_mongodb_connection_string with your MongoDB URI.

## Usage
* Start the server: npm start
* The server will start running at http://localhost:3000.

## API Documentation
* ### Get All Products
    **Endpoint:** /api/products
    **Method:** GET<br>
    **Response:** <br><br>
    &nbsp;&nbsp;[<br>
     &nbsp;&nbsp;&nbsp;&nbsp; {<br>
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   "_id": "product_id",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "name": "Product Name",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "quantity": 10,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "price": 99.99,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "image": "product_image_url",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "createdAt": "2024-07-12T10:00:00.000Z",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  "updatedAt": "2024-07-12T12:00:00.000Z"<br>
      &nbsp;&nbsp;&nbsp;&nbsp;},<br>
     &nbsp;&nbsp;&nbsp;&nbsp; ...<br>
    &nbsp;&nbsp;]<br>
* ### Get a Product by ID
    **Endpoint:** /api/products/:id<br>
    **Method:** GET<br>
    **Response:**<br>
    &nbsp;&nbsp;{<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"_id": "product_id",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"name": "Product Name",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"quantity": 10,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"price": 99.99,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"image": "product_image_url",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"createdAt": "2024-07-12T10:00:00.000Z",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"updatedAt": "2024-07-12T12:00:00.000Z"<br>
    &nbsp;&nbsp;}<br>
* ### Create a Product
    **Endpoint:** /api/products<br>
    **Method:** POST<br>
    **Request Body:**<br>
    &nbsp;&nbsp;{<br>
     &nbsp;&nbsp;&nbsp;&nbsp; "name": "Product Name",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"quantity": 10,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"price": 99.99,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"image": "product_image_url"<br>
    &nbsp;&nbsp;}<br>
    **Response:**<br>
    &nbsp;&nbsp;{<br>
     &nbsp;&nbsp;&nbsp;&nbsp; "_id": "product_id",<br>
     &nbsp;&nbsp;&nbsp;&nbsp; "name": "Product Name",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"quantity": 10,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"price": 99.99,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"image": "product_image_url",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"createdAt": "2024-07-12T10:00:00.000Z",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"updatedAt": "2024-07-12T10:00:00.000Z"<br>
    &nbsp;&nbsp;}<br>
* ### Update a Product
    **Endpoint:** /api/products/:id<br>
    **Method:** PUT<br>
    **Request Body:** Any of the following fields can be updated:<br>
    &nbsp;&nbsp;{<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"name": "Updated Product Name",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"quantity": 20,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"price": 149.99,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"image": "updated_product_image_url"<br>
    &nbsp;&nbsp;}<br>
    **Response:**<br>
    &nbsp;&nbsp;{<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"_id": "product_id",<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"name": "Updated Product Name",<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"quantity": 20,<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"price": 149.99,<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"image": "updated_product_image_url",<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"createdAt": "2024-07-12T10:00:00.000Z",<br>
     &nbsp;&nbsp;&nbsp;&nbsp;"updatedAt": "2024-07-12T11:00:00.000Z"<br>
    &nbsp;&nbsp;}<br>
* ### Delete a Product
    **Endpoint:** /api/products/:id<br>
    **Method:** DELETE<br>
    **Response:** <br>
    &nbsp;&nbsp;{<br>
    &nbsp;&nbsp;&nbsp;&nbsp; "message": "Product deleted successfully"<br>
    &nbsp;&nbsp;}<br>
## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.
