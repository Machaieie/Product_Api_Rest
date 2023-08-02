# Products API with Spring Boot

This is a Spring Boot-based product management API that allows basic CRUD (Create, Read, Update, Delete) operations for products. Each product has a unique identifier (ID), a descriptive name, and an associated value.

## Requirements

Before running the API, make sure you have the following dependencies installed:

- Java JDK 11 or above
- Maven

## How to Run the API

1. Clone this repository to your local machine:

```
git clone https://github.com/Machaieie/Product_Api_Rest.git
```

2. Navigate to the project directory:

```
cd Product_Api_Rest.git
```

3. Compile the project using Maven:

```
mvn clean install
```

4. Start the embedded Spring Boot server:

```
mvn spring-boot:run
```

The API will be available at `http://localhost:8080`.

## Endpoints

The API provides the following endpoints for managing products:

- **GET /products**: Retrieves all registered products.
- **GET /products/{id}**: Retrieves a specific product based on the provided ID.
- **POST /products**: Creates a new product with the data provided in the request body (JSON).
- **PUT /products/{id}**: Updates the data of an existing product based on the provided ID.
- **DELETE /products/{id}**: Removes a product based on the provided ID.

## JSON Format

The JSON objects for creating and updating products should follow this format:

```json
{
  "id": 1,
  "name": "Product A",
  "value": 19.99
}
```

The `id` field is optional when creating a new product, as it will be automatically assigned by the system.

## Response Status

The API returns the following status codes:

- 200 OK: Request successful.
- 201 Created: Product created successfully.
- 204 No Content: Request successful, but no content to return (usually in deletions).
- 400 Bad Request: Validation error or invalid format in the request.
- 404 Not Found: Product not found.
- 500 Internal Server Error: Internal server error.

## Usage Examples

### Create a new product

```http
POST /products
Content-Type: application/json

{
  "name": "New Product",
  "value": 25.99
}
```

### Update an existing product

```http
PUT /products/1
Content-Type: application/json

{
  "id": 1,
  "name": "Updated Product",
  "value": 29.99
}
```

### Delete a product

```http
DELETE /products/1
```

## Final Remarks

This API is a simple implementation and can be used as a starting point for more complex projects. Feel free to make improvements, add additional features, or adapt it to the specific needs of your project.

If you have any questions or encounter issues, don't hesitate to open an issue in this repository. Contributions are always welcome!

Enjoy the API and happy product management!

