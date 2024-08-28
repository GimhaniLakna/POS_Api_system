# POS System 

POS has a feature that tracks your business’s analytics performance and operations. Think of the back end as a “backstage”. In the “backstage” of your POS, you can check your data, customer insights and reports.  Real Time Data In your POS’s back-end, you can review your business’s data in real time.

# Introduction

The POS System is designed to manage customer orders, inventory, and sales efficiently. This backend was developed using Jakarta EE, with a focus on maintaining a proper layered architecture, applying best practices in coding, and ensuring secure database interactions.

# Architecture

The application follows a layered architecture, comprising:

* Presentation Layer: Interfaces with the frontend via RESTful APIs.
* Business Logic Layer: Contains the core logic, ensuring that business rules are enforced.
* Data Access Layer: Handles database operations using native SQL queries, abstracted via Data Access Objects (DAOs).


# Database Configuration

Database connectivity is managed using JNDI. The persistence.xml or relevant configuration files are set up to ensure secure and efficient access to the MySQL database.

* Database: MySQL
* JNDI Name: java:/comp/env/jdbc/posDB
* Schema: The database schema includes tables for Customers, Orders, Items, and Order Details.

# API Endpoints

The backend exposes a set of RESTful APIs to perform operations like creating orders, updating customer information, and managing inventory. Detailed documentation for these endpoints is provided here.

Example API Endpoints:

### *  Customer Operations

* GET /posApi/customers
* POST /posApi/customers
* PUT /posApi/customers/{customerId}
* DELETE /posApi/customers/{customerId}


### * Item Operation
* GET /posApi/item
* POST /posApi/item
* PUT /posApi/item/{id}
* DELETE /posApi/item/{id}

### * Order Operations

* GET /posApi/orders
* POST /posApi/orders

# Logging

Logging is implemented using Jakarta EE's built-in logging mechanisms. Different logging levels (INFO, DEBUG, ERROR) are applied appropriately to capture application events, aiding in monitoring and troubleshooting.


