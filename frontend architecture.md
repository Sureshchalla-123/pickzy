# 🧱 Frontend Structure — Pages, Routes & Components

---

## 🧱 1. Pages (Full Screens)

These are full pages rendered via routes.

| Page Name                    | Purpose                                                    |
| ---------------------------- | ---------------------------------------------------------- |
| HomePage                     | Display banner + categories + trending products            |
| ProductsPage                 | List all products with search, filter, sorting, pagination |
| ProductDetailsPage           | Show single product info + add to cart                     |
| SignupPage                   | New user registration                                      |
| LoginPage                    | User login                                                 |
| CartPage                     | View cart items + update quantities + checkout button      |
| CheckoutPage                 | Shipping details + payment method + order summary          |
| PaymentPage                  | Payment process (Stripe/Razorpay)                          |
| OrderSuccessPage             | Order placed confirmation                                  |
| OrdersPage                   | Order history for user                                     |
| ProfilePage                  | User profile + address + password change                   |
| WishlistPage (optional)      | User-saved items                                           |
| SearchResultsPage (optional) | Separate search experience                                 |
| AdminDashboard               | Admin statistics overview                                  |
| AdminProductsPage            | Product list with CRUD                                     |
| AdminAddProductPage          | Create new product                                         |
| AdminEditProductPage         | Edit existing product                                      |
| AdminOrdersPage              | Manage orders                                              |
| AdminUsersPage               | Manage users                                               |

---

## 🔁 2. Routes Structure

Route → Corresponding Page

### 🧑‍💻 Public Routes

/ → HomePage
/products → ProductsPage
/products/:id → ProductDetailsPage
/search → SearchResultsPage (optional)
/signup → SignupPage
/login → LoginPage

shell
Copy code

### 🔐 Protected User Routes (login required)

/cart → CartPage
/checkout → CheckoutPage
/payment → PaymentPage
/order-success → OrderSuccessPage
/orders → OrdersPage
/profile → ProfilePage
/wishlist → WishlistPage (optional)

pgsql
Copy code

### 🛡️ Admin Routes (admin role required)

/admin/dashboard → AdminDashboard
/admin/products → AdminProductsPage
/admin/products/add → AdminAddProductPage
/admin/products/edit/:id → AdminEditProductPage
/admin/orders → AdminOrdersPage
/admin/users → AdminUsersPage

markdown
Copy code

---

## 🧩 3. Components (Reusable UI Blocks)

These are UI building blocks used across pages.

### 🔹 Layout Components

- Navbar
- Footer
- Sidebar (for admin)
- ProtectedRoute (User auth guard)
- AdminRoute (Admin auth guard)

### 🔹 Shared Components

- Button
- Input
- TextArea
- Select
- Modal
- Loader
- Error
- EmptyState

### 🔹 E-Commerce Components

- ProductCard
- ProductGrid
- ProductCarousel (banner slider)
- CategoryCard
- RatingStars
- ReviewCard
- AddToCartButton
- CartItem
- CartSummary
- OrderCard
- SearchBar
- FilterSidebar

### 🔹 Forms

- LoginForm
- SignupForm
- CheckoutForm
- AddressForm
- PaymentForm
- ProductForm (admin)
- UserForm (admin update user details)

---

## ⚙️ Suggested Folder Structure (Best Practice)

src/
components/
common/
layout/
product/
cart/
admin/
pages/
Home/
Products/
ProductDetails/
Login/
Signup/
Cart/
Checkout/
Payment/
Orders/
Profile/
Wishlist/
Admin/
routes/
AppRoutes.jsx
ProtectedRoute.jsx
AdminRoute.jsx
context/ or store/
utils/
services/ (API calls e.g., authAPI, productAPI)
assets/

yaml
Copy code

---
