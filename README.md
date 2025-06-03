# Hotel_Management
# Bluebird Hotel Management System

A comprehensive web-based hotel management system built with PHP and MySQL for managing hotel operations including room bookings, payments, staff management, and customer registration.

## 🏨 Features

### Core Functionality
- **Room Management**: Manage different room types (Single, Superior, Deluxe, Guest House) with various bedding options
- **Booking System**: Handle room reservations with check-in/check-out dates
- **Payment Processing**: Track and manage payment details for bookings
- **Staff Management**: Maintain staff records with roles and responsibilities
- **User Authentication**: Secure login system for both customers and employees
- **Customer Registration**: User signup and account management

### Room Types Available
- **Single Room**: Basic accommodation
- **Superior Room**: Enhanced comfort with Single/Double/Triple/Quad bedding
- **Deluxe Room**: Premium accommodation with various bedding options
- **Guest House**: Extended stay options with flexible bedding arrangements

## 🛠️ Technology Stack

- **Backend**: PHP
- **Database**: MySQL
- **Server**: Apache/Nginx (XAMPP/WAMP compatible)
- **Frontend**: HTML, CSS, JavaScript (assumed)

## 📋 Database Schema

### Tables Overview

#### 1. `emp_login`
Employee authentication system
- `empid`: Employee ID (Primary Key)
- `Emp_Email`: Employee email address
- `Emp_Password`: Employee password

#### 2. `signup`
Customer registration system
- `UserID`: User ID (Primary Key)
- `Username`: Customer name
- `Email`: Customer email
- `Password`: Customer password

#### 3. `room`
Room inventory management
- `id`: Room ID (Primary Key)
- `type`: Room type (Single, Superior, Deluxe, Guest House)
- `bedding`: Bedding configuration (Single, Double, Triple, Quad)

#### 4. `roombook`
Booking management system
- `id`: Booking ID (Primary Key)
- `Name`: Customer name
- `Email`: Customer email
- `Country`: Customer country
- `Phone`: Contact number
- `RoomType`: Type of room booked
- `Bed`: Bedding preference
- `Meal`: Meal plan selected
- `NoofRoom`: Number of rooms
- `cin`: Check-in date
- `cout`: Check-out date
- `nodays`: Number of days
- `stat`: Booking status

#### 5. `payment`
Payment processing and tracking
- `id`: Payment ID (Primary Key)
- `Name`: Customer name
- `Email`: Customer email
- `RoomType`: Room type
- `Bed`: Bedding type
- `NoofRoom`: Number of rooms
- `cin`: Check-in date
- `cout`: Check-out date
- `noofdays`: Duration of stay
- `roomtotal`: Room charges
- `bedtotal`: Bedding charges
- `meal`: Meal plan
- `mealtotal`: Meal charges
- `finaltotal`: Total amount

#### 6. `staff`
Staff management system
- `id`: Staff ID (Primary Key)
- `name`: Staff member name
- `work`: Job role (Manager, Cook, Helper, Cleaner, etc.)

## 🚀 Installation & Setup

### Prerequisites
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache/Nginx web server
- XAMPP/WAMP (for local development)

### Installation Steps

1. **Clone/Download the project**
   ```bash
   git clone [your-repository-url]
   cd bluebird-hotel-management
   ```

2. **Database Setup**
   ```sql
   -- Import the database
   mysql -u root -p < bluebirdhotel.sql
   ```
   
   Or using phpMyAdmin:
   - Open phpMyAdmin
   - Create new database named `bluebirdhotel`
   - Import `bluebirdhotel.sql` file

3. **Configure Database Connection**
   - Update `config.php` with your database credentials:
   ```php
   $server = "localhost";
   $username = "bluebird_user";  // or your MySQL username
   $password = "password";       // or your MySQL password
   $database = "bluebirdhotel";
   ```

4. **Web Server Setup**
   - Place project files in your web server directory
   - For XAMPP: `htdocs/bluebird-hotel/`
   - For WAMP: `www/bluebird-hotel/`

5. **Access the Application**
   - Open browser and navigate to: `http://localhost/bluebird-hotel/`

## 👥 Default Login Credentials

### Admin/Employee Login
- **Email**: `Admin@gmail.com`
- **Password**: `1234`

### Sample Customer Account
- **Username**: `Tushar Pankhaniya`
- **Email**: `tusharpankhaniya2202@gmail.com`
- **Password**: `123`

## 📝 Usage

### For Customers
1. **Registration**: Create account through signup page
2. **Room Booking**: Select room type, dates, and preferences
3. **Payment**: Complete booking with payment details
4. **Booking Management**: View and manage reservations

### For Staff/Admin
1. **Login**: Access admin panel with employee credentials
2. **Room Management**: Add/edit/delete room configurations
3. **Booking Management**: View and manage customer bookings
4. **Staff Management**: Manage staff records and roles
5. **Payment Tracking**: Monitor payment transactions

## 🏗️ Project Structure

```
bluebird-hotel-management/
├── config.php                 # Database configuration
├── bluebirdhotel.sql          # Database schema and sample data
├── index.php                  # Main page (assumed)
├── admin/                     # Admin panel files
├── customer/                  # Customer interface files
├── includes/                  # Common PHP includes
├── css/                       # Stylesheets
├── js/                        # JavaScript files
├── images/                    # Image assets
└── README.md                  # This file
```

## 🔧 Configuration

### Database Configuration
The system uses MySQL database with the following configuration:
- **Database**: `bluebirdhotel`
- **User**: `bluebird_user`
- **Password**: `password`
- **Host**: `localhost`

### Room Pricing (Customizable)
- Room charges calculated based on room type and duration
- Additional charges for premium bedding options
- Meal plan options with separate pricing

## 🚨 Security Notes

1. **Change Default Passwords**: Update all default login credentials
2. **Database Security**: Use strong passwords for database users
3. **Input Validation**: Ensure all user inputs are properly validated
4. **SQL Injection Prevention**: Use prepared statements for database queries
5. **Session Management**: Implement proper session handling for user authentication

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📋 Future Enhancements

- [ ] Online payment gateway integration
- [ ] Email notifications for bookings
- [ ] Advanced reporting system
- [ ] Mobile responsive design
- [ ] Multi-language support
- [ ] Room availability calendar
- [ ] Customer feedback system
- [ ] Inventory management for amenities

## 🐛 Troubleshooting

### Common Issues

1. **Database Connection Failed**
   - Check MySQL service is running
   - Verify credentials in `config.php`
   - Ensure database `bluebirdhotel` exists

2. **Permission Errors**
   - Check file permissions for web server access
   - Ensure database user has proper privileges

3. **Page Not Loading**
   - Verify web server is running
   - Check file paths and directory structure

