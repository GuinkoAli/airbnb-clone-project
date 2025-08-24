# airbnb-clone-project

## Team Roles
* **Backend Developer**
  - Responsible for implementing API endpoints, database schemas, and business logic.
* **Database Administrator**
  -Manages database design, indexing, and optimizations.
* **DevOps Engineer**
  - Handles deployment, monitoring, and scaling of the backend services Facilitates cooperation between development and operations teams and Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery.
* **QA Engineer**
  - The job of a quality assurance engineer is to vEnsures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack 
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

## Database Design
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

## Feature Breakdown
Below are the core features implemented in the Airbnb Clone project, along with a short description of how each contributes to the overall system.

* **User Management**
    - Handles user registration, login, and profile management. Each user can own properties, make bookings, write reviews, and process payments. -  - Authentication and authorization ensure secure access to the platform.

* **Property Management**
  - Allows users to list new properties with details like title, description, price, and location. 
  - Property owners can manage (create, edit, delete) their listings, and other users can browse and book them.

* **Booking System**
  - Enables users to make reservations for available properties by selecting start and end dates.
  - The booking system ensures that date conflicts are avoided and keeps track of the booking status for both guests and hosts.

* **Payment Processing**
  - Facilitates payments linked to specific bookings. 
  - Users can pay securely using supported payment methods, and each payment is recorded with its status for transparency and auditing.

* **Reviews and Ratings**
  - Allows users to leave ratings and written feedback on properties they have booked. 
  = This helps improve trust in the platform and provides valuable insights to other users.

* **Notifications & Asynchronous Tasks**
  - Uses Celery for background tasks such as sending booking confirmations, payment notifications, or other asynchronous processes, improving overall user experience.

* **API and Data Querying**
  - The backend provides RESTful API endpoints built with Django REST Framework, as well as flexible GraphQL queries for retrieving data efficiently. - This allows frontend applications to interact seamlessly with the backend.

* **Deployment & DevOps**
  - The project uses Docker for containerization and has CI/CD pipelines to automate testing and deployment. This ensures consistent environments, quick delivery of updates, and easier scalability.

* **Caching and Performance**
  - Redis is used to cache frequently accessed data and manage user sessions efficiently. This reduces response times and improves the overall performance of the application.
