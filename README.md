# Booking Appointment System

A simple web application for managing user appointments with CRUD operations. Built with Node.js, Express, MySQL, and Bootstrap.

## Features

- Create new user appointments
- View all registered users
- Delete user appointments
- Update existing appointments
- Responsive UI with Bootstrap
- RESTful API endpoints
- MySQL database integration with Sequelize ORM
- Form validation
- Error handling

## Prerequisites

Before running this project, make sure you have the following installed:

- Node.js (v12 or higher)
- MySQL Server
- npm (Node Package Manager)

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd booking-appointment
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   ```bash
   cp .env.example .env
   ```

   Update the `.env` file with your MySQL credentials and other configuration.

4. Set up MySQL database:

   - Create a new database
   - Update database configuration in `config/database.js`

5. Run database migrations:

   ```bash
   npm run migrate
   ```

6. Start the server:

   ```bash
   npm start
   ```

7. Access the application:
   Open your browser and navigate to `http://localhost:3000`

## API Endpoints

| Method | Endpoint         | Description       |
| ------ | ---------------- | ----------------- |
| POST   | `/api/users`     | Create a new user |
| GET    | `/api/users`     | Get all users     |
| PUT    | `/api/users/:id` | Update a user     |
| DELETE | `/api/users/:id` | Delete a user     |

### Request & Response Examples

#### Update User

```
PUT /api/users/:id
Content-Type: application/json

{
  "name": "John Doe Updated",
  "email": "john.updated@example.com",
  "phone": "9876543210"
}
```

Response:

```json
{
  "message": "User updated successfully",
  "user": {
    "id": 1,
    "name": "John Doe Updated",
    "email": "john.updated@example.com",
    "phone": "9876543210"
  }
}
```

## Technologies Used

- Node.js
- Express.js
- MySQL
- Sequelize ORM
- Bootstrap 5
- JavaScript
- HTML/CSS

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
