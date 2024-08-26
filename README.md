**Badoy Car Rental System**

This README provides an overview of the Car Rental System, a Python application that uses SQLite3 as its database. The system allows admin to manage car rentals, including adding new cars, editing and deleting cars, renting cars to customers, and returning rented cars.

Features

- **Add New Cars**: Admin can add new cars to the inventory.
- **Edit Cars**: Admin can edit details cars to the inventory.
- **Delete Cars**: Admin can delete cars to the inventory that are now longer available in the car rental.
- **Return Cars**: Admin will return rented cars once validated that the car is returened safely.
- **View Rented Cars**: Admins can view all currently rented cars and all cars in the car rental.
- **Rent Cars**: Customers can rent available cars and system will display the total amount due to pay.
- **View Available Cars**: Admin and Users can view all available cars for rent.
- **View Rented Cars**: Admins can view all currently rented cars.

## Technologies Used

- **Python**: The main programming language used for the application logic.
- **SQLite3**: A lightweight, disk-based database that doesn’t require a separate server process.

## Getting Started

### Prerequisites

- Python 3.x installed on your system.
- SQLite3 installed on your system (usually comes with Python).

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/car-rental-system.git
   cd car-rental-system
   ```

2. **Install Required Libraries**:
   Ensure you have SQLite3 installed. You can install any additional Python packages using pip if needed:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up the Database**:
   Run the following command to set up the SQLite database:
   ```bash
   python setup_database.py
   ```

## Usage

1. **Run the Application**:
   Start the application by running the main Python script:
   ```bash
   python main.py
   ```

2. **Navigate the Menu**:
   Follow the on-screen prompts to navigate through the options:
   - Add a new car
   - Rent a car
   - Return a car
   - View available cars
   - View rented cars

## Database Schema

The SQLite database consists of the following tables:

- **cars**:
  - `id` (INTEGER): Primary key.
  - `make` (TEXT): The make of the car.
  - `model` (TEXT): The model of the car.
  - `yearmake` (INTEGER): The manufacturing year.
  - `price_per_day` (REAL): The price per day.
  - `mileage` (INTEGER): The mileage of the car in KM.
  - `available_now` (TEXT): Availability status.
  - `min_rent` (INTEGER): The mininum rent days.
  - `max_rent` (INTEGER): The maximum rent days.
 
- **users**:
  - `username` (TEXT): Primary key.
  - `password` (TEXT): The password of the user.
  - `first_name` (TEXT): The first name of the user.
  - `last_name` (TEXT): The last name of the user.
  - `address` (TEXT): The address of the user.
  - `contact_number` (TEXT): The contact numner of the user.
  - `email` (TEXT): The email of the user.

- **rentals**:
  - `id` (INTEGER): Primary key.
  - `car_id` (INTEGER): Foreign key referencing cas.
  - `username` (TEXT): Foreign key referencing users.
  - `customer_name` (TEXT): Name of the customer renting the car.
  - `start_date` (TEXT): Date when the car was rented.
  - `end_date` (TEXT): Date when the car is returned (nullable).
  - `total_price` (REAL): The price to pay.
  - `status` (TEXT): Status of the rental.

## Contributing

1. **Fork the Repository**: Create your own fork of the project.
2. **Create a Feature Branch**: 
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit Your Changes**: 
   ```bash
   git commit -m 'Add some feature'
   ```
4. **Push to the Branch**: 
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request**: Submit your changes for review.

## License

This project is licensed under the GNU GENERAL PUBLIC LICENSE. See the `LICENSE` file for more details.

## Credits
Developed by: Marc A. Badoy
Email: 270515588@yoobeestudent.ac.nz
GitHub: https://github.com/Mabadoy
LinkedIn: https://www.linkedin.com/in/marc-badoy-33831316b/
This README provides a comprehensive guide for both users and programmers to understand, install, and use the Badoy Car Rental System.
It includes all the requested sections, detailing the installation process, system components, usage instructions, known issues, licensing terms, and developer credits, specifically tailored for a Python command-line application using SQLite3.

This README provides a comprehensive guide to setting up and using the Car Rental System. Adjust the content as necessary to fit your specific project details and requirements.
