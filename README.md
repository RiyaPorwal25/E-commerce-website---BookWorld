# E-commerce website  BookWorld
It is  a fully functional e-commerce website called BookWorld where users can browse a wide range of books, register, log in, manage their shopping cart, and proceed to checkout. The platform is built using Django for the backend, MySQL for database management, and Bootstrap for the responsive front-end design.

Key Features:

• User Authentication: Implemented user registration and login functionality with form validation and password security features.

• Product Catalog: Developed a product catalog where users can browse books with details like title, price, and author. Used Django’s ORM for data handling.

• Shopping Cart: Built a shopping cart where users can add, update, and remove items. Integrated functionality for increasing or decreasing quantities and calculating total prices.

• Checkout Process: Designed a secure checkout page where users can review their cart and proceed to payment. Integrated payment gateway (Razorpay) for transaction processing.

• Responsive Design: Utilized Bootstrap 5 for responsive design ensuring an optimal experience across devices (desktop, tablet, mobile).

• Dynamic Cart Summary: Created a dynamic cart summary that updates in real-time, displaying total price and conversion to INR.

• Database Management: Utilized MySQL for managing products, orders, and user information. Implemented efficient queries for retrieving and updating data.


Technologies Used:

• Backend: Django, Python

• Frontend: HTML, CSS, Bootstrap

• Database: MySQL

• Version Control: Git


Detailed description of code:

1. Views (Django Views)

    1.Product List View:
   
    • This view renders a list of products available in the store.
   
    • Each product displays its image, name, price, and author.
   
    • There's a link to add the product to the cart.
   
   
    2. Registration View:
   
    • Handles the registration of new users.
   
    • It includes validation and feedback on the form submission (e.g., passwords do not match).
   
    • Utilizes Django's built-in messages to show errors (e.g., invalid username or password).


    3. Login View:
   
    • Handles user login with username and password.
   
    • On successful login, users are redirected to a page or dashboard.
   
    • It displays messages if login fails, such as "incorrect username or password."


    4. Shopping Cart View:
       
    • Displays the products in the cart.
   
    • Each product in the cart shows the image, name, price, quantity, and total price for the quantity selected.
   
    • The user can increase/decrease quantity or remove items from the cart.
   
    • A cart summary section calculates the total price, which can be converted to INR.


    6. Checkout Page View:
   
    • A page that leads to the checkout process (likely to process payments).
   
    • Option to proceed with the purchase.


3. Models (Django Models)

  Product Model:
  
      • The product model defines the structure of products in the store.
      
      • Each product includes fields like name, price, author, description, and an image.
      
      • The image field stores the image file for each product.

   
  Cart Model:
  
      • A model to represent the user's cart.
      
      • It keeps track of the product, quantity, and user in the cart.
      
      • The cart model connects to the product model and stores the user’s current cart data.

      
  Order Model:

      • Stores the user’s order information.
      
      • Tracks order details like product items, payment status, shipping details, etc.
      
      • It can be used to create and track completed orders.


3. Forms (Django Forms)

  1. Registration Form:
  
     • The form that captures user details for registration.
     
     • Fields include username, first_name, last_name, email, password, and confirm_password.
     
     • It has validation logic to ensure the data is entered correctly, including password confirmation and username uniqueness.

     
  2. Login Form:
  
     • A simple form where users enter their username and password to authenticate.
     
     • It provides basic form validation.


4. Templates (HTML & Django Template Language)
   
  1.Product List Template:
  
    • Displays the list of products in the store.
    
    • Shows the image, name, price, and author of each product.
    
    • Includes an "Add to Cart" button that allows users to add products to the shopping cart.
   
  2.Registration Template:
  
    • Contains a registration form where new users can sign up.
    
    • Displays any error messages if user registration fails (e.g., invalid username, password mismatch).
    
    • Links to the login page for existing users.
    
  3. Login Template:
     
    • Contains a login form for users to authenticate.
    
    • Shows error messages (if any) and includes links to register or reset the password.
    
    •Styled using Bootstrap for responsive design.

  4.Shopping Cart Template:
  
    • Displays the user’s cart with items added.
    
    • Each item shows the name, price, image, and quantity.
    
    • Users can update the quantity or remove items from the cart.
    
    • Provides a "Proceed to Checkout" button.



5. URLs (Django URL Routing)
   
• The views mentioned above are mapped to specific URLs using Django’s urls.py configuration. These URLs direct users to:

    • The product listing page.
    
    • The user registration page.
    
    • The login page.
    
    • The shopping cart page.
    
    • The checkout page.


7. Settings (settings.py)
   
  • Security & Debugging:
  
      • SECRET_KEY for encryption and hashing.
      
      • DEBUG is set to True, which is useful during development (should be set to False in production).
   
  • Database:
  
      • Configures MySQL as the backend database.
      
      • Defines connection settings like NAME, USER, PASSWORD, and PORT.

  • Static and Media Files:
  
      • Defines directories for serving static files (STATIC_URL and STATICFILES_DIRS) and media files (MEDIA_URL and MEDIA_ROOT).

  • Authentication:
  
      • Configures the login URL (LOGIN_URL) and redirect URL after logging out (LOGOUT_REDIRECT_URL).
        


Responsibilities:

• Designed and implemented user authentication and authorization features, ensuring secure login and registration.

• Developed cart functionalities including adding/removing products, quantity updates, and price calculations.

• Integrated the Razorpay payment gateway for processing payments securely.

• Ensured responsive and user-friendly design across various devices using Bootstrap.

• Managed database schemas for storing products, orders, and user data.

• Applied Django’s model-view-template (MVT) architecture to maintain code modularity and scalability.


Outcome:

• Successfully launched the BookWorld website with seamless integration between front-end and back-end.

• Provided users with a secure and intuitive platform to purchase books, with an easy-to-navigate interface and real-time cart updates.
