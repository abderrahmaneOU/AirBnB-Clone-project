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
- `user_id`: Foreign key referencing the User who made the booking  
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
