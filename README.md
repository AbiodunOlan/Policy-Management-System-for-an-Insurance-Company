# Policy-Management-System-for-an-Insurance-Company

# Insurance Management System

## Overview

The Insurance Management System is designed to manage policyholders, insurance products, and payments. It allows policy managers to perform various tasks such as adding and suspending policyholders, registering new members, and managing policy products.

## Features

- **Policyholder Management**
  - Register new policyholders
  - Suspend and reactivate policyholders
  - Display policyholder details along with their payment history

- **Product Management**
  - Create new insurance products
  - Update existing products
  - Suspend products

- **Payment Management**
  - Process premium payments
  - Track payment history

## Project Structure


Certainly! Here is an example of a README file for your insurance management system:

README.md
markdown
Copy code
# Insurance Management System

## Overview

The Insurance Management System is designed to manage policyholders, insurance products, and payments. It allows policy managers to perform various tasks such as adding and suspending policyholders, registering new members, and managing policy products.

## Features

- **Policyholder Management**
  - Register new policyholders
  - Suspend and reactivate policyholders
  - Display policyholder details along with their payment history

- **Product Management**
  - Create new insurance products
  - Update existing products
  - Suspend products

- **Payment Management**
  - Process premium payments
  - Track payment history

## Project Structure

insurance_management/
│
├── policyholder.py # Policyholder class definition
├── product.py # Product class definition
├── payment.py # Payment class definition
├── policyholder_manager.py # Manager for policyholder operations
├── product_manager.py # Manager for product operations
├── payment_manager.py # Manager for payment operations
└── main.py # Demonstration script



## Classes

### Policyholder

Represents a policyholder.

#### Attributes:
- `policyholder_id` (int): Unique identifier for the policyholder
- `name` (str): Name of the policyholder
- `contact_info` (str): Contact information of the policyholder
- `status` (str): Status of the policyholder (Active/Suspended)
- `payments` (list): List of payments made by the policyholder

#### Methods:
- `suspend()`: Suspend the policyholder
- `reactivate()`: Reactivate the policyholder
- `add_payment(payment)`: Add a payment to the policyholder's record
- `__str__()`: String representation of the policyholder

### Product

Represents an insurance product.

#### Attributes:
- `product_id` (int): Unique identifier for the product
- `name` (str): Name of the product
- `description` (str): Description of the product
- `premium_amount` (float): Premium amount of the product
- `status` (str): Status of the product (Active/Suspended)

#### Methods:
- `update(name, description, premium_amount)`: Update the product details
- `suspend()`: Suspend the product
- `__str__()`: String representation of the product

### Payment

Represents a payment made by a policyholder.

#### Attributes:
- `payment_id` (int): Unique identifier for the payment
- `policyholder_id` (int): ID of the policyholder who made the payment
- `amount` (float): Amount paid
- `date` (str): Date of the payment
- `payment_method` (str): Payment method used
- `status` (str): Status of the payment (Completed)

#### Methods:
- `__str__()`: String representation of the payment

## Managers

### PolicyholderManager

Manages policyholder operations.

#### Methods:
- `register_policyholder(name, contact_info)`: Register a new policyholder
- `suspend_policyholder(policyholder_id)`: Suspend a policyholder
- `reactivate_policyholder(policyholder_id)`: Reactivate a policyholder
- `get_policyholder(policyholder_id)`: Get a policyholder by ID

### ProductManager

Manages product operations.

#### Methods:
- `create_product(name, description, premium_amount)`: Create a new product
- `update_product(product_id, name, description, premium_amount)`: Update an existing product
- `suspend_product(product_id)`: Suspend a product
- `get_product(product_id)`: Get a product by ID

### PaymentManager

Manages payment operations.

#### Methods:
- `process_payment(policyholder_id, amount, date, payment_method)`: Process a new payment
- `send_reminder(policyholder_id)`: Send a payment reminder (placeholder)
- `apply_penalty(policyholder_id, penalty_amount)`: Apply a penalty (placeholder)

## Demonstration

### Setup

Ensure all class files and manager files are in the same directory. Run `main.py` to see the demonstration of the system.

### Running the Demo

```sh
python main.ipynb
