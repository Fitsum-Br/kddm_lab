# KDDM Assignment 1: Data Quality & ERD Analysis

## Short Note Answers

### a. Customer Identifiers
The `customers` table contains two identifier columns: `customer_id` and `customer_unique_id`. 
* `customer_id` is a transaction-specific key generated per order (a returning customer receives a new `customer_id` for every distinct order).
* `customer_unique_id` represents the actual individual customer across all historical orders.
* **Selection:** `customer_unique_id` must be used to count total unique users accurately; relying on `customer_id` would overcount repeat buyers.

### b. Junction Table
* **Junction Table:** `order_items`
* **Relationships Resolved:** It resolves the many-to-many relationship between `orders` and `products` (as well as `sellers`). A single order can contain multiple product line items, and a single product can appear in many distinct orders.

### c. Data Strictness vs. Diagram Cardinality
* **Stricter Data Relationship:** The relationship from `orders` to `customers` is stricter in practice because our anti-join verification returned 0 orphan orders (every order points to a valid customer record).
* **Justified Diagram Circle:** The optional circle ("zero or many") on the relationship between `orders` and `order_items` is justified because data quality checks identified 775 orders with no associated order items (e.g., canceled or unavailable order statuses).