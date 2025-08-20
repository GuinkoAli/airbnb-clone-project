# airbnb-clone-project

# Team Roles
* **Backend Developer**
  - Responsible for implementing API endpoints, database schemas, and business logic.
* **Database Administrator**
  -Manages database design, indexing, and optimizations.
* **DevOps Engineer**
  - Handles deployment, monitoring, and scaling of the backend services Facilitates cooperation between development and operations teams and Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery.
* **QA Engineer**
  - The job of a quality assurance engineer is to vEnsures the backend functionalities are thoroughly tested and meet quality standards.

# Technology Stack 
* **Django**
  - A high-level Python web framework used for building the RESTful API.
* **Django REST Framework**
  - Provides tools for creating and managing RESTful APIs.
* **PostgreSQL**
  - A powerful relational database used for data storage.
* **GraphQL**
  - Allows for flexible and efficient querying of data.
* **Celery**
  - For handling asynchronous tasks such as sending notifications or processing payments.
* **Redis**
  - Used for caching and session management.
* **Docker**
  - Containerization tool for consistent development and deployment environments.
* **CI/CD Pipelines**
  - Automated pipelines for testing and deploying code changes. 

# Database Design
* **Users**
  - id, name, email, password
  - A user can own properties, make bookings, leave reviews, and make payments.
* **Properties**
  - id, user_id, title, description, price, location
  - A user can own many properties that other users can reiew and book.
* **Bookings**
  - id, user_id, property_id, start_date, end_date, status
  - A user can book a property that is connected to another user with only one payment.
- **Payments**
  - id, booking_id, amount, method, status
  - A payment is linked to one booking.
* **Reviews**
  - id, user_id, property_id, rating, comment
  - A review is attached to a particular user and a property.
