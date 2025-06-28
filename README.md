# airbnb-clone-project
Project Initialization
## Team Roles

To ensure the successful delivery of the Airbnb Clone Project, the following roles and responsibilities are defined:

- **Backend Developer**: Implements server-side logic, builds and manages APIs, and handles integration with the database and external services.
- **Frontend Developer**: Develops the user interface and experience using HTML/CSS and JavaScript frameworks such as React.
- **Database Administrator (DBA)**: Designs, manages, and optimizes the relational database (PostgreSQL), ensuring data security and performance.
- **DevOps Engineer**: Handles CI/CD pipelines, containerization with Docker, and deploys the application to the cloud or local servers.
- **Quality Assurance (QA) Engineer**: Tests features, reports bugs, and ensures all components work as expected.
- **Project Manager**: Oversees the development process, assigns tasks, tracks progress, and ensures milestones are met.

## Technology Stack

This project uses a modern full-stack web development toolkit:

- **Python**: The primary programming language for backend development.
- **Django**: A high-level Python web framework used to build robust and scalable backend APIs.
- **PostgreSQL**: A powerful and open-source relational database used for storing application data.
- **GraphQL**: A query language for APIs that provides flexible and efficient data fetching.
- **HTML/CSS/JavaScript**: Core frontend technologies for building and styling user interfaces.
- **React** (optional): A JavaScript library for building dynamic and reusable frontend components.
- **Docker**: Used to containerize the application and ensure consistency across development and production environments.
- **GitHub Actions**: Automates testing, linting, and deployment workflows as part of the CI/CD process.


## Database Design

The database will be structured around the following core entities:

### 1. Users
- `id`: Unique identifier
- `full_name`: Full name of the user
- `email`: Email address
- `password`: Encrypted user password
- `role`: Either "host" or "guest"

### 2. Properties
- `id`: Unique identifier
- `title`: Name or description of the property
- `location`: Address or city
- `price_per_night`: Rental cost
- `host_id`: References the user who owns the property

### 3. Bookings
- `id`: Unique identifier
- `user_id`: References the guest who made the booking
- `property_id`: References the booked property
- `check_in`: Start date of the stay
- `check_out`: End date of the stay

### 4. Reviews
- `id`: Unique identifier
- `user_id`: Reviewer (guest)
- `property_id`: Reviewed property
- `rating`: Score (e.g., 1–5)
- `comment`: Text review

### 5. Payments
- `id`: Unique identifier
- `booking_id`: References the booking
- `amount`: Total amount paid
- `payment_date`: Date of payment
- `method`: Payment method (e.g., credit card, PayPal)

### Entity Relationships

- A **user** can act as a **host** (listing properties) or a **guest** (making bookings).
- A **host** can have many **properties**.
- A **guest** can make multiple **bookings**.
- Each **booking** is for one **property** and made by one **guest**.
- Each **property** can receive many **reviews** from guests.
- Each **booking** is linked to one **payment** transaction.

## Feature Breakdown

The Airbnb Clone project includes the following key features:

### 1. User Management
Allows users to register, log in, and manage their profiles. Users can act as either guests (to book properties) or hosts (to list properties).

### 2. Property Listings
Hosts can create, update, and delete property listings, including descriptions, prices, and photos. Listings are displayed for guests to browse.

### 3. Booking System
Enables guests to book available properties for a selected date range. Bookings are stored and managed in the database, linked to both the property and the user.

### 4. Reviews and Ratings
After completing a stay, guests can leave reviews and ratings for properties. This builds trust and provides valuable feedback to other users.

### 5. Payment Integration
Guests can securely pay for bookings using supported payment methods. Payments are linked to bookings and recorded for tracking.

### 6. Search and Filter
Guests can search for properties by location, price, date, and other filters to find listings that suit their needs.

### 7. Admin Dashboard
Admins can manage users, listings, and resolve issues (optional feature depending on team scope).


