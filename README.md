# airbnb-clone-project

## Brief Overview
The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security.

## Project Goals

1. User Management: Implement a secure system for user registration, authentication, and profile management.
2. Property Management: Develop features for property listing creation, updates, and retrieval.
3. Booking System: Create a booking mechanism for users to reserve properties and manage booking details.
4. Payment Processing: Integrate a payment system to handle transactions and record payment details.
5. Review System: Allow users to leave reviews and ratings for properties.
6. Data Optimization: Ensure efficient data retrieval and storage through database optimizations


## Team Roles

### 1. Business Analyst:
* Understands customer's business process.
* Translates customer business needs into requirements.

### 2. Product Owner
* Holds responsibility for a product vision and evolution.
* Makes sure the finall product meets customer requirements.

### 3. Project Manager
* Makes sure a product or its part is delivered on time and within budget.
* Manages and motivates the software development team.
* Distribution of tasks across team members, planning work activities, and updating project status.

### 4. UI/UX designer
* Transforms a product vision into user-friendly designs
* Creates user journeys for the best user experience and highest conversion rates.

### 5. Software Architect
* Designs high-level software architecture.
* Selects the appropriate tools to implement the product vision.
* Sets up code quality standards and performs code reviews.

### 6. Software Developer
* Engineers and stabalizes the product.
* Solves any technical problems  emerging during the development lifecycle.
* **Front-end developers**: create the part of the application that the user interact with
* **Back-end developers**: Responsible for implementing API endpoints, database schemas, and business logic.
* **Full-stack developers**: Handle both the frontend and the backend.
### 7. Database Administrator: 
* Manages database design, indexing, and optimizations.
### 8. DevOps Engineer: 
* Handles deployment, monitoring, and scaling of the backend services.
### 9. QA Engineer: 
* Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack
The project uses the following technologies:
1. Django: A web framework for creating RESTful API's
2. Django REST Framework: Provides tools for creating and managing RESTful API's
3. PostgreSQL: Powerful relational database used for data storage.
4. GraphQL: Allows flexible and efficient querying of data.
5. Celery: Used for handling asynchrounous tasks such as sending notifications or processing payments.
6. Redis: used for caching and session management.
7. Docker: Containerization tool for consistent development and deployment environements.
8. CI/CD pipelines: Automated pipelines for testing and deploying code changes.

## Database Design
The following are the entities, fields and relationships.

### 1. Users
- **Fields**:
  - `user_id`: Unique identifier for the user
  - `name`: Name of the user
  - `email`: Email address
  - `phone`: Contact number
- **Relationships**:
  - Can have multiple bookings
  - Can own multiple properties (shared ownership possible)

### 2. Properties
- **Fields**:
  - `property_id`: Unique identifier for the property
  - `address`: Location of the property
  - `type`: Type of property (e.g., apartment, house)
  - `owner_ids`: List of user IDs owning the property
- **Relationships**:
  - Associated with multiple bookings

### 3. Bookings
- **Fields**:
  - `booking_id`: Unique identifier for the booking
  - `user_id`: ID of the user who made the booking
  - `property_id`: ID of the booked property
  - `date`: Date of the booking
  - `status`: Booking status (e.g., confirmed, canceled)
- **Relationships**:
  - Linked to one user
  - Linked to one property

### 4. Reviews
- **Fields**:
  - `review_id`: Unique identifier for the review
  - `user_id`: ID of the user who left the review
  - `property_id`: ID of the property being reviewed
  - `rating`: Numeric rating (e.g., 1–5 stars)
  - `comments`: User's feedback
- **Relationships**:
  - Posted by one user
  - Associated with one property

### 5. Payments
- **Fields**:
  - `payment_id`: Unique identifier for the payment
  - `booking_id`: ID of the booking tied to the payment
  - `amount`: Payment amount
  - `payment_date`: Date of payment
  - `method`: Payment method (e.g., credit card, PayPal)
- **Relationships**:
  - Linked to one booking

 ## Feature Breakdown
### 1. User Management
Handles user registration, login, and profile management. This feature ensures a secure and personalized experience by allowing users to manage their accounts and access tailored functionalities with ease.

### 2. Property Management
Enables users to list, update, and manage properties. This feature supports co-ownership, allowing multiple users to share property ownership, and helps property owners showcase their offerings effectively.

### 3. Booking System
Facilitates the creation, management, and tracking of bookings. Users can reserve properties, view booking statuses, and manage their schedules seamlessly through this streamlined system.

### 4. Review System
Allows users to leave feedback and rate properties. By building trust through transparency, this feature helps potential users make informed decisions based on previous reviews and ratings.

### 5. Payment Processing
Handles secure transactions for bookings. It supports multiple payment methods, ensures reliable payment processing, and enhances user confidence with its seamless integration and ease of use.

