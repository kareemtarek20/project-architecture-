# ✨ Inventory Management System

A robust Inventory Management System built with **Laravel 10** and **MySQL**, designed to streamline your inventory tracking, sales, and purchasing processes.

![Dashboard](https://github.com/user-attachments/assets/1df45f1d-aaed-4299-9b90-35e7f47dc7ea)

## 🗂️ Database Design

The system is structured using a clear and efficient database schema:

![Database Diagram](https://github.com/fajarghifar/inventory-management-system/assets/71541409/0c7d4163-96f5-4724-8741-4615e52ecf98)

## 🌟 Key Features

-   **POS (Point of Sale)**
-   **Orders**
    -   Pending Orders
    -   Complete Orders
    -   Pending Payments
-   **Purchases**
    -   All Purchases
    -   Approval Process
    -   Purchase Reports
-   **Products Management**
-   **Customer Records**
-   **Supplier Management**

## 🚀 Quick Start

Follow these steps to set up the project locally:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/fajarghifar/inventory-management-system
    ```

2. **Navigate to the project folder:**

    ```bash
    cd inventory-management-system
    ```

3. **Install PHP dependencies:**

    ```bash
    composer install
    ```

4. **Copy `.env` configuration:**

    ```bash
    cp .env.example .env
    ```

5. **Generate application key:**

    ```bash
    php artisan key:generate
    ```

6. **Configure the database in the `.env` file** with your local credentials.

7. **Run database migrations and seed sample data:**

    ```bash
    php artisan migrate:fresh --seed
    ```

8. **Link storage for media files:**

    ```bash
    php artisan storage:link
    ```

9. **Install JavaScript and CSS dependencies:**

    ```bash
    npm install && npm run dev
    ```

10. **Start the Laravel development server:**

    ```bash
    php artisan serve
    ```

11. **Login using the default admin credentials:**

    - **Email:** `admin@admin.com`
    - **Password:** `password`

12. **Design patterns used in this project**
    Design patterns are typical solutions to common problems in software design. They represent best practices refined over time. Here's an overview of **four main types of design patterns**:

---

### 1. **Creational Design Patterns**

**Purpose**: Deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

**Common Patterns**:

* **Singleton**: Ensures a class has only one instance and provides a global point of access.
* **Factory Method**: Defines an interface for creating an object, but lets subclasses alter the type of objects that will be created.
* **Abstract Factory**: Produces families of related or dependent objects without specifying their concrete classes.
* **Builder**: Separates the construction of a complex object from its representation.
* **Prototype**: Creates new objects by copying an existing object, known as the prototype.

---

### 2. **Structural Design Patterns**

**Purpose**: Deal with object composition—how objects can be combined to form larger structures.

**Common Patterns**:

* **Adapter**: Allows incompatible interfaces to work together.
* **Bridge**: Separates an object’s abstraction from its implementation.
* **Composite**: Composes objects into tree structures to represent part-whole hierarchies.
* **Decorator**: Adds new functionality to an object dynamically.
* **Facade**: Provides a simplified interface to a complex subsystem.
* **Flyweight**: Reduces the cost of creating and manipulating a large number of similar objects.
* **Proxy**: Provides a surrogate or placeholder for another object.

---

### 3. **Behavioral Design Patterns**

**Purpose**: Focus on communication between objects and how responsibilities are distributed.

**Common Patterns**:

* **Observer**: Defines a dependency between objects so that when one changes state, all its dependents are notified.
* **Strategy**: Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
* **Command**: Encapsulates a request as an object, allowing parameterization of clients with queues, requests, or logs.
* **Chain of Responsibility**: Passes requests along a chain of handlers until one handles it.
* **Mediator**: Centralizes complex communication between related objects.
* **State**: Allows an object to alter its behavior when its internal state changes.
* **Template Method**: Defines the program skeleton in a method, deferring some steps to subclasses.

---

### 4. **Concurrency (or Multithreading) Patterns**

**Purpose**: Deal with multi-threaded programming paradigms and safe concurrent access to resources.

**Common Patterns**:

* **Thread Pool**: Manages a pool of worker threads to perform tasks, improving performance.
* **Producer-Consumer**: Coordinates communication between threads that produce and consume data.
* **Read-Write Lock**: Allows concurrent read access but exclusive write access to resources.
* **Double-Checked Locking**: Reduces the overhead of acquiring a lock by first testing the locking criterion.

---

13. **project structure**

---

### 🔍 **Detailed Explanation of Key Folders**

#### 1. **`app/Models`**

* Houses **Eloquent models**, which represent database tables.
* Encapsulates the data and behavior of the data (e.g., `Product`, `User`, `Order`).
* Often includes relationships like `hasMany`, `belongsTo`.

#### 2. **`app/Http/Controllers`**

* Contains controllers that handle **request-response logic**.
* Typically grouped by domain (e.g., `InventoryController`, `AuthController`).
* Controllers use **dependency injection** to work with services or repositories.

#### 3. **`app/Http/Requests`**

* Custom **Form Request** classes for input validation logic.
* Keeps controllers clean by offloading validation responsibilities.

#### 4. **`app/Services`**

* Contains **service layer classes** that encapsulate business logic.
* Promotes separation of concerns, e.g., `InventoryService`, `OrderService`.

#### 5. **`app/Repositories`**

* Implements the **Repository Pattern** to abstract database operations.
* Interfaces may be defined for flexibility and testing (`ProductRepositoryInterface`, `ProductRepository`).

#### 6. **`app/Observers`**

* Contains **event observers** that listen to model events (e.g., on create/update/delete).
* Useful for side effects like logging or notifications.

#### 7. **`app/Policies`**

* Used for **authorization logic** (who can do what).
* Integrated with Laravel’s `Gate` and `Auth` system.

---

### 📁 Other Important Directories

#### 8. **`routes/`**

* Defines all the **application routes**.
* Common files:

  * `web.php`: Routes for web interface.
  * `api.php`: Routes for API requests.
  * `channels.php`: Broadcast channels.
  * `console.php`: Artisan commands.

#### 9. **`resources/views/`**

* Blade template files (Laravel's templating engine).
* Can be structured by domain (e.g., `products/index.blade.php`).

#### 10. **`config/`**

* All **configuration files** (app, database, mail, etc).
* You can add your own config files (e.g., `config/inventory.php`).

#### 11. **`database/`**

* Contains database-related files:

  * `migrations/`: Version-controlled schema changes.
  * `seeders/`: Populate tables with default data.
  * `factories/`: Used for testing and dummy data.

#### 12. **`tests/`**

* Unit and feature tests go here.
* Encourages **test-driven development (TDD)**.

---

### ✅ Benefits of This Structure

* **Scalability**: Easy to expand by adding new services, controllers, or features.
* **Maintainability**: Separation of concerns helps manage large codebases.
* **Reusability**: Logic encapsulated in services and repositories can be reused across controllers or commands.
* **Testability**: Clean separation makes unit testing simpler.

---




