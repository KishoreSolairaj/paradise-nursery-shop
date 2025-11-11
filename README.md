# 🌿 Paradise Nursery - E-Commerce Plant Shop

**Where Green Meets Serenity**

A modern, fully-functional e-commerce web application for browsing and purchasing plants online. Built with React and Redux for seamless state management and real-time shopping cart updates.



---

## ✨ Features

### Product Catalog
- **5 Plant Categories**: Air Purifying, Aromatic Fragrant, Insect Repellent, Medicinal, and Low Maintenance
- **30+ Products**: Each with image, name, description, and price
- **Responsive Grid Layout**: Clean, modern product card design

### Shopping Cart Functionality
- ✅ Add products to cart with one click
- ✅ Real-time cart item count badge
- ✅ Increment/Decrement item quantities
- ✅ Remove items from cart
- ✅ Automatic total and subtotal calculations
- ✅ Button state management (prevents duplicate additions)
- ✅ Continue shopping without losing cart state

### User Experience
- Intuitive navigation between product listing and cart
- Visual feedback for user actions
- Disabled buttons after adding to cart
- Dynamic button text ("Add to Cart" → "Added to Cart")
- Real-time price calculations

---

## 🛠 Technologies Used

- **React** (v18+) - UI component library
- **Redux Toolkit** - State management
- **React-Redux** - React bindings for Redux
- **CSS3** - Styling and layouts
- **JavaScript (ES6+)** - Application logic

---

## 📁 Project Structure

```
paradise-nursery/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── ProductList.jsx       # Product listing page
│   │   ├── ProductList.css       # Product page styles
│   │   ├── CartItem.jsx          # Shopping cart component
│   │   ├── CartItem.css          # Cart styles
│   │   ├── CartSlice.jsx         # Redux slice for cart
│   │   └── store.js              # Redux store configuration
│   ├── App.js                    # Main app component
│   ├── App.css                   # App styles
│   └── index.js                  # Entry point
├── package.json
└── README.md
```

---

## 🚀 Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/KishoreSolairaj/paradise-nursery.git
   cd paradise-nursery
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Required packages** (if not already included)
   ```bash
   npm install @reduxjs/toolkit react-redux
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open in browser**
   ```
   http://localhost:3000
   ```

---

## 📖 Usage

### Browsing Products
1. The landing page displays all plant categories
2. Scroll through different categories to explore plants
3. Each plant card shows:
   - Plant image
   - Name
   - Description
   - Price
   - Add to Cart button

### Adding to Cart
1. Click "Add to Cart" on any product
2. Button changes to "Added to Cart" and becomes disabled
3. Cart icon badge updates with total item count

### Managing Cart
1. Click the cart icon in the navigation bar
2. View all items in your cart with:
   - Product images and details
   - Quantity controls (+/- buttons)
   - Individual item subtotals
   - Total cart amount
3. Adjust quantities or remove items as needed
4. Click "Continue Shopping" to return to products

---

## 🧩 Components Overview

### ProductList.jsx
**Purpose**: Main product listing page

**Key Features**:
- Displays all plant categories and products
- Handles "Add to Cart" functionality
- Shows cart item count badge
- Manages navigation between views

**Key Functions**:
- `handleAddToCart(product)` - Adds product to Redux store
- `calculateTotalQuantity()` - Calculates total items in cart
- `handleCartClick()` - Navigates to cart view
- `handleContinueShopping()` - Returns to product listing

---

### CartItem.jsx
**Purpose**: Shopping cart management

**Key Features**:
- Displays all cart items
- Calculates totals and subtotals
- Increment/Decrement quantities
- Remove items from cart

**Key Functions**:
- `calculateTotalAmount()` - Calculates total cart cost
- `calculateTotalCost(item)` - Calculates individual item subtotal
- `handleIncrement(item)` - Increases item quantity
- `handleDecrement(item)` - Decreases quantity or removes item
- `handleRemove(item)` - Removes item from cart

---

### CartSlice.jsx
**Purpose**: Redux state management for shopping cart

**State Structure**:
```javascript
{
  items: [
    {
      name: "Snake Plant",
      image: "https://...",
      cost: "$15",
      quantity: 2
    }
  ]
}
```

**Reducers**:
- `addItem` - Adds new item or increments existing quantity
- `removeItem` - Removes item from cart
- `updateQuantity` - Updates item quantity

---

### store.js
**Purpose**: Redux store configuration

Configures the Redux store with the cart reducer and exports it for use throughout the application.

---

## 🔄 Redux State Management

### Data Flow

```
User Action (Add to Cart)
    ↓
ProductList Component
    ↓
dispatch(addItem(product))
    ↓
CartSlice Reducer
    ↓
Redux Store Updated
    ↓
Components Re-render
    ↓
UI Updates (Cart Badge, Totals, etc.)
```

### Actions Available

1. **addItem(product)**
   - Payload: `{ name, image, cost }`
   - Adds product or increments quantity

2. **removeItem(name)**
   - Payload: `name` (string)
   - Removes item from cart

3. **updateQuantity({ name, quantity })**
   - Payload: `{ name, quantity }`
   - Updates item quantity

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Your Name**
- GitHub: [@KishoreSolairaj](https://github.com/KishoreSolairaj)
- LinkedIn: [Your LinkedIn](www.linkedin.com/in/kishoresolairaj)
- Email: talktokishoresolairaj@gmail.com

---

**Made with 💚 and React**

*Paradise Nursery - Bringing nature to your doorstep*
