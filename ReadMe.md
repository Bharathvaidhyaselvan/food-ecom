# iFood - Online Food Delivery Web Application

## Overview

iFood is an online food delivery web application built with HTML, CSS, and JavaScript. It is designed to showcase a complete solution for managing and displaying food products, orders, and categories—focusing on popular South Indian cuisine. The project is divided between a public-facing site and an administration panel, both of which work together to deliver a seamless and responsive user experience.

## Features

### Public Site

- **Responsive Design:**  
  The home page (`index.html`) provides a fully responsive layout with distinct sections including Hero, About, Features, Products, Gallery, and Footer.
- **Dynamic Product Display:**  
  The products section dynamically loads product data from a JSON file, ensuring that items such as images, titles, descriptions, and prices are rendered correctly.
- **Navigation:**  
  Easy-to-use navigation links lead users to Home, About, Menu, and Contact sections.

### Admin Panel

#### Dashboard (`admin/dashboard.html`)

- **Statistics Overview:**  
  Displays key metrics such as total orders, total products, number of categories, and revenue.
- **Recent Orders List:**  
  Provides a quick view of recent orders with details like order ID, customer name, product name, status, and total.

- **Order Management:**  
  Allows administrators to view order details, update status, and delete orders through modal dialogs.

#### Product Management (`admin/products.html`)

- **Product Listing:**  
  Retrieves and displays a paginated list of products from `products.json`. Each product card shows an image, title (using `product.title`), category, price, and status.
- **Edit & Delete Operations:**  
  Administrators can edit product details or delete products using modals. The code uses event listeners on dynamically generated edit and delete buttons.
- **Pagination:**  
  Implements pagination to manage large sets of products efficiently by calculating the total number of pages based on the products per page.

#### Category Management (`admin/categories.html`)

- **Default Categories Setup:**  
  Defines Indian-themed default categories (e.g., Breakfast, South Indian, Snacks, Desserts, Beverages) with respective images and attributes.
- **LocalStorage Integration:**  
  Uses localStorage to persist category data across admin sessions. The code reinitializes categories on page load to ensure updates are reflected.

## Data Files

- **products.json:**  
  Contains an array of product objects with properties such as `id`, `title`, `description`, `price`, `rating`, `category`, `status`, and `image`. This file is consumed both by the public site and the admin product management page.
- **Default Categories Data:**  
  Embedded in the categories management script and stored in localStorage (under the key `admin_categories`).

## Technologies Used

- **HTML5, CSS3 & JavaScript:**  
  For building the responsive layouts, dynamic interactions, and DOM manipulation.
- **Fetch API:**  
  To load JSON data (products and categories) dynamically.
- **LocalStorage:**  
  For storing persistent data such as admin categories.
- **Responsive Web Design:**  
  Ensures the application works seamlessly on various devices and screen sizes.

## Setup Instructions

1. **Clone the Repository:**
   ```sh
   git clone <repository-url>
   ```
2. **Directory Structure:**

   - `/index.html` — Public site homepage.
   - `/products.json` — JSON file containing product data.
   - `/admin/dashboard.html` — Admin dashboard page.
   - `/admin/products.html` — Admin product management page.
   - `/admin/categories.html` — Admin category management page.

3. **Running the Application:**
   - Open `index.html` in your browser for the public-facing site.
   - For administrative functions, open the respective files under `/admin/` (e.g., `admin/products.html`).
   - Use Visual Studio Code with Live Server or open files directly in a browser.

## Future Enhancements

- **Backend API Integration:**  
  Transition from static JSON/localStorage to a dynamic backend service for real-time product, order, and category management.
- **Admin Authentication:**  
  Implement a secure login system to restrict administrative functionalities to authorized users.
- **Improved UI/UX:**  
  Enhance the visual design and user interactions with advanced styling and animations.

## Conclusion

iFood provides a robust platform combining a public front-end with a comprehensive admin panel for managing online food delivery services. By leveraging modern web technologies and following a modular design approach, the application delivers a responsive, user-friendly experience optimized for both customers and administrators.
