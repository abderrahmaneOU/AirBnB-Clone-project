# AirBnB-Clone-project

## Team Roles

**Backend Developer**  
Responsible for building and maintaining the server-side logic of the application. They create APIs, manage data flow, and ensure the performance and scalability of backend services.

**Frontend Developer**  
Implements the visual and interactive elements that users interact with. They connect the frontend interface to backend services using APIs.

**Database Administrator (DBA)**  
Designs, implements, and maintains the database system. Ensures data integrity, security, and performance.

**DevOps Engineer**  
Manages deployment, CI/CD pipelines, and system monitoring. They automate workflows and ensure smooth integration between development and operations.

**UI/UX Designer**  
Focuses on the user experience and interface design. Ensures the app is user-friendly, accessible, and visually appealing.

**Project Manager**  
Coordinates the project timeline, team responsibilities, and deliverables. Ensures that the project meets its goals on time and within scope.

## Technology Stack

**Python**  
The main programming language used to build the application’s backend logic and core functionalities.

**Flask**  
A lightweight web framework used for creating RESTful APIs and handling HTTP requests and responses.

**Jinja2**  
A templating engine used with Flask to dynamically generate HTML pages.

**SQLite / MySQL**  
Relational databases used to store and manage application data such as users, listings, and reservations.

**SQLAlchemy**  
An Object Relational Mapper (ORM) that allows developers to interact with the database using Python objects instead of raw SQL.

**HTML/CSS**  
Used to structure and style the frontend interface of the application.

**JavaScript**  
Adds interactivity to the user interface and enhances the user experience on the frontend.

**Git**  
A version control tool is used to manage code changes and facilitate collaboration with other developers.

**GitHub**  
The hosting platform for the project’s codebase and documentation, enabling collaboration and version tracking.

## Database Design

### Entities and Fields

**User**  
- `id`: Unique identifier  
- `name`: Full name of the user  
- `email`: Email address  
- `password`: Hashed password  
- `created_at`: Account creation date  

**Property**  
- `id`: Unique identifier  
- `owner_id`: Foreign key referencing the User  
- `title`: Name of the listing  
- `location`: Address or city  
- `price_per_night`: Cost to stay per night  

**Booking**  
- `id`: Unique identifier  
- `user_id`: Foreign key referencing the Usare er who made the booking  
- `property_id`: Foreign key referencing the Property  
- `start_date`: Start date of the stay  
- `end_date`: End date of the stay  

**Review**  
- `id`: Unique identifier  
- `user_id`: Foreign key referencing the reviewer  
- `property_id`: Foreign key referencing the Property  
- `rating`: Score from 1 to 5  
- `comment`: Written feedback  

**Payment**  
- `id`: Unique identifier  
- `booking_id`: Foreign key referencing the Booking  
- `amount`: Payment total  
- `payment_date`: Date of transaction  
- `status`: Paid, pending, or failed  

### Relationships

- A **User** can own multiple **Properties**.  
- A **User** can make multiple **Bookings**.  
- A **Property** can have multiple **Bookings** and **Reviews**.  
- A **Booking** is linked to one **User** and one **Property**.  
- A **Payment** is associated with one **Booking**.  
- A **User** can leave multiple **Reviews** on different Properties.

## Feature Breakdown

**User Management**  
Allows users to sign up, log in, and manage their profile information. This ensures that each user has a secure, personalized experience on the platform.

**Property Management**  
Enables hosts to list their properties with details like title, location, price, and images. It provides tools to update or remove listings as needed.

**Booking System**  
Let users browse available properties and book them for specific dates. The system checks for availability, calculates the total price, and confirms bookings.

**Review System**  
Allows guests to leave reviews and ratings after their stay. This fosters trust within the community and enables others to make informed decisions.

**Payment Processing**  
Handles secure payment transactions for bookings. Ensures that payments are recorded and associated with the correct bookings.

**Search and Filter**  
Users can search for properties based on location, date, price, and more. This improves usability by helping users quickly find suitable listings.

**Responsive Interface**  
A user-friendly web interface that works across devices. It ensures a smooth experience whether accessed on desktop, tablet, or mobile.

## API Security

**Authentication**  
We will implement user authentication to verify the identity of users before allowing access to protected resources. This helps ensure that only registered users can log in and interact with their accounts securely.

**Authorization**  
Authorization will be used to control what authenticated users can do. For example, only property owners can modify their listings, and only users who made a booking can leave a review. This prevents unauthorized actions on sensitive data.

**Rate Limiting**  
Rate limiting will be enforced to prevent abuse such as spamming the API with excessive requests. It protects the system from performance degradation and denial-of-service attacks.

**Data Validation and Sanitization**  
All input data will be validated and sanitized to prevent common vulnerabilities like SQL injection and cross-site scripting (XSS). This ensures that only clean, expected data is processed.

**Secure Communication (HTTPS)**  
The application will enforce HTTPS for all communication between clients and the server. This encrypts sensitive data such as login credentials and payment information to prevent eavesdropping.

## CI/CD Pipeline

**What is CI/CD?**  
CI/CD stands for Continuous Integration and Continuous Deployment. It is a development practice where code changes are automatically tested and deployed to production. This helps teams deliver updates faster and with fewer bugs.

**Importance for the Project**  
Implementing a CI/CD pipeline ensures that the Airbnb Clone project remains stable and up-to-date. It automates repetitive tasks like testing, building, and deploying, which reduces human error and speeds up the development process.

**Tools Used**  
- **GitHub Actions**: Automates workflows such as running tests and deploying code after each push.  
- **Docker**: Containerizes the application, making it easy to deploy in different environments.  
- **pytest or unittest**: Used for automated testing of the application logic.  
- **Heroku or AWS**: Can be used to deploy the final application to a live environment.
