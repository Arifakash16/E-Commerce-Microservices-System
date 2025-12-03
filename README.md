# E-Commerce-Microservices-System

1. Catalog Service – README (Short Version)
Catalog Service

The Catalog Service manages all product-related data for the E-Commerce Microservices System.
It provides APIs for creating, updating, deleting, and retrieving product information.

Key Features

- Add, update, delete, and fetch product details

- Product categories, descriptions, images, prices

- Built using .NET Core Web API

- Stores product data in MongoDB (or SQL depending on implementation)

Endpoints (Example)

- GET /api/catalog/products

- GET /api/catalog/products/{id}

- POST /api/catalog/products

- PUT /api/catalog/products/{id}

- DELETE /api/catalog/products/{id}

Technologies

- .NET Core Web API

- MongoDB / SQL

- Clean Architecture

2. Basket Service – README (Short Version)
Basket Service

The Basket Service handles customer shopping carts.
It manages cart items, quantities, total price calculation, and applies discounts before checkout.

Key Features

- Add, update, and remove items from a user’s basket

- Retrieve basket by customer username

- Apply discount codes (via Discount Service)

- Save/restore cart state

- Built using .NET Core Web API

Endpoints (Example)

- GET /api/basket/{username}

- POST /api/basket

- DELETE /api/basket/{username}

- POST /api/basket/apply-discount

Technologies

- .NET Core Web API

- Redis (commonly used for basket storage)

- gRPC / HTTP integration with Discount Service

3. Discount Service – README (Short Version)
Discount Service

The Discount Service provides coupon-based discount management.
Basket Service calls this service to get discount values.

Key Features

- Create, update, delete, and retrieve discount coupons

- Apply coupon to user’s basket

- Supports percentage or fixed-amount discounts

- Built using .NET Core Web API or gRPC

Endpoints (Example)

- GET /api/discount/{code}

- POST /api/discount

- PUT /api/discount/{code}

- DELETE /api/discount/{code}

Technologies

- .NET Core Web API

- PostgreSQL / SQL database

- gRPC communication
