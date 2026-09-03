# 🛍️ ShopVerse — React E-Commerce Store

A modern and responsive **e-commerce web application built with React.js and Vite**. ShopVerse provides a smooth shopping experience with product browsing, search and category filtering, cart management, checkout, order confirmation, and user authentication UI.

The project is built as a frontend-focused application and uses **React Context API and LocalStorage** for state and data persistence.

---

## ✨ Features

### 🏠 Home Page

* Modern hero section
* Featured shopping experience
* Responsive design
* Call-to-action buttons
* Store highlights

### 🛒 Product Management

* Product listing
* Product cards
* Product categories
* Product ratings
* Product descriptions
* Product images
* Add-to-cart functionality
* Add-product interface

### 🔍 Search & Filtering

* Search products by name
* Search products by description
* Filter products by category
* Dynamic category generation

### 🛍️ Shopping Cart

* Add products to cart
* Increase/decrease quantity
* Remove products
* Calculate total items
* Calculate total price
* Persistent cart using LocalStorage

### 💳 Checkout

* Customer information form
* Contact information
* Address details
* Payment method selection
* Order notes
* Form validation

### 📦 Order Management

* Generate order number
* Save order information
* Order confirmation page
* Display order details after checkout
* Clear cart after successful order

### 🔐 Authentication UI

* Login form
* Registration form
* Email validation
* Password validation
* Confirm password validation
* LocalStorage-based user state

### 📱 Responsive UI

* Responsive navigation
* Mobile-friendly layout
* Responsive product grid
* Tailwind CSS styling

---

## 🧰 Tech Stack

| Technology            | Purpose                      |
| --------------------- | ---------------------------- |
| **React.js**          | Frontend UI                  |
| **Vite**              | Development & build tool     |
| **JavaScript (ES6+)** | Application logic            |
| **React Router DOM**  | Page routing                 |
| **Context API**       | Global cart state            |
| **LocalStorage**      | Client-side data persistence |
| **Tailwind CSS**      | Styling                      |
| **PostCSS**           | CSS processing               |

---

## 📂 Project Structure

```text
store-app/
│
├── public/
│
├── src/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── Hero.jsx
│   │   ├── ProductList.jsx
│   │   ├── ProductCard.jsx
│   │   ├── AddProduct.jsx
│   │   ├── Cart.jsx
│   │   ├── OrderForm.jsx
│   │   └── Footer.jsx
│   │
│   ├── context/
│   │   └── CartContext.jsx
│   │
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Products.jsx
│   │   ├── About.jsx
│   │   ├── Contact.jsx
│   │   └── Login.jsx
│   │
│   ├── App.jsx
│   ├── main.jsx
│   ├── index.css
│   └── config.js
│
├── index.html
├── package.json
├── package-lock.json
├── postcss.config.js
├── tailwind.config.js
└── README.md
```

---

## 🔄 Application Flow

```text
                    ┌───────────────┐
                    │    main.jsx   │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │    App.jsx    │
                    └───────┬───────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
          Navbar         Products       Footer
                            │
                            ▼
                      ProductList
                            │
                            ▼
                      ProductCard
                            │
                            ▼
                        Add Cart
                            │
                            ▼
                     CartContext
                            │
                            ▼
                       Shopping Cart
                            │
                            ▼
                         Checkout
                            │
                            ▼
                      Order Success
```

---

## 🧠 State Management

The application uses **React Context API** to manage shopping-cart state globally.

The `CartContext` handles:

```text
products
cartItems
addToCart()
removeFromCart()
updateQuantity()
clearCart()
getTotalPrice()
getTotalItems()
addProduct()
```

This allows components such as `ProductCard`, `ProductList`, `Cart`, and `OrderForm` to access shared application state without manually passing props through multiple levels.

---

## 💾 LocalStorage

ShopVerse uses browser LocalStorage to persist application data.

The cart is stored locally so that users can retain their cart after refreshing the page.

```text
React State
     │
     ▼
useEffect()
     │
     ▼
LocalStorage
```

On application startup:

```text
LocalStorage
     │
     ▼
React State
     │
     ▼
Application
```

---

## 🧭 Routes

| Route            | Description          |
| ---------------- | -------------------- |
| `/`              | Home page            |
| `/products`      | Product listing      |
| `/about`         | About page           |
| `/contact`       | Contact page         |
| `/login`         | Login / Registration |
| `/cart`          | Shopping cart        |
| `/order`         | Checkout             |
| `/order-success` | Order confirmation   |
| `/add-product`   | Product management   |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Navigate into the project

```bash
cd store-app
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

The application will be available at the local URL provided by Vite, usually:

```text
http://localhost:5173
```

### 5. Create a production build

```bash
npm run build
```

### 6. Preview the production build

```bash
npm run preview
```

---

## 🛒 Sample Products

The application includes sample products such as:

* 🎧 Wireless Headphones
* 🎒 Classic Leather Backpack
* ⌚ Smart Watch Pro
* 💡 Minimal Desk Lamp

Products contain information such as:

```text
Name
Description
Price
Category
Rating
Image
```

---

## 🔐 Authentication

The current project contains a frontend authentication interface with:

* Sign In
* Register
* Email validation
* Password validation
* Confirm password validation

User information is currently handled on the client side using LocalStorage.

> **Note:** This implementation is intended for frontend/demo purposes. A production application should use a secure backend authentication system with password hashing, sessions/JWT, and proper authorization.

---

## 💳 Payment

The checkout page provides a payment-method interface, but the project does not currently process real payments.

For production, a payment provider such as Stripe or another supported gateway could be integrated with a backend.

---

## 🔮 Future Improvements

The project can be extended with:

* [ ] Node.js + Express backend
* [ ] MongoDB database
* [ ] Real user authentication
* [ ] JWT authentication
* [ ] Admin dashboard
* [ ] Real product CRUD
* [ ] Product image upload
* [ ] Product details page
* [ ] Wishlist
* [ ] Order history
* [ ] Real payment integration
* [ ] Inventory management
* [ ] Customer reviews
* [ ] Email notifications
* [ ] Backend API
* [ ] Cloud deployment
* [ ] Loading states
* [ ] Error handling
* [ ] Protected routes

---

## 🎯 Learning Objectives

This project demonstrates practical use of:

* React components
* JSX
* Props
* `useState`
* `useEffect`
* Context API
* React Router
* Event handling
* Forms
* Form validation
* Array methods
* Conditional rendering
* LocalStorage
* Responsive UI
* Tailwind CSS
* Component-based architecture

---

## 📸 Screenshots

Add your application screenshots here:

```text
screenshots/
├── home.png
├── products.png
├── product-details.png
├── cart.png
├── checkout.png
└── order-success.png
```

Example:

```markdown
![Home Page](screenshots/home.png)

![Products](screenshots/products.png)

![Shopping Cart](screenshots/cart.png)

![Checkout](screenshots/checkout.png)
```

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/new-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add new feature"
```

5. Push the branch

```bash
git push origin feature/new-feature
```

6. Open a Pull Request

---

## 📄 License

This project is available for educational and portfolio purposes.

---

## 👨‍💻 Author

**Nadeem Ashraf**

Software Engineer | React.js Developer

GitHub: **nadeem-ashraf-dev**

---

⭐ If you find this project useful, consider giving it a star on GitHub!
