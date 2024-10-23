# E-Commerce Store

A simple e-commerce store built with React that allows users to browse products, add them to a cart, and proceed to checkout.

## Features

- **Product Listing**: View a list of products fetched from an API.
- **Shopping Cart**: Add products to your cart and view the total price.
- **Checkout**: Fill in your details and submit an order.
- **Responsive Design**: The application is fully responsive for both mobile and desktop users.

## Technologies Used

- React
- Bootstrap (for styling)
- React Router (for navigation)
- Context API (for state management)


Usage
Home Page: The home page displays a list of products. Click on "Add to Cart" to add items to your cart.
Cart Page: Navigate to the cart page to view selected items, total price, and options to remove items.
Checkout Page: Fill out the checkout form to complete your purchase.


Components Overview
App: Main application component that sets up routing and context.
ProductList: Fetches and displays a list of products.
ProductCard: Displays individual product details and an "Add to Cart" button.
Cart: Displays items in the cart and the total price.
Checkout: Handles user input for completing the purchase.


Workflow
The workflow of the application is structured as follows:

Data Fetching:
Upon loading the ProductList component, an API call is made to https://fakestoreapi.com/products to fetch product data.
The fetched data is stored in the component's state and is then passed to child components for rendering.

Displaying Products:
The ProductList component maps over the fetched products and renders a ProductCard for each product.
Each ProductCard displays product information and has an "Add to Cart" button.

Managing Cart State:
The cart's state is managed using React's Context API in the CartContext.
When a user clicks "Add to Cart," the product is added to the cart state, and the total item count is updated.

Cart Functionality:
The Cart component displays the current items in the cart, total price, and provides an option to remove items.
Users can navigate to the checkout page from the cart.

Checkout Process:
The Checkout component collects user details (name, address, payment) and displays an order summary.
Upon submission, the cart is cleared after a brief delay, allowing the user to see the confirmation.
