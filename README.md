# 🛒 Shopping Cart Application

A modern, responsive e-commerce shopping cart built with React, Redux Toolkit, and Tailwind CSS. Features real-time cart management, smooth animations, and a clean user interface.

![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-1.9.7-764ABC?style=for-the-badge&logo=redux&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.2.7-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-6.9.0-CA4245?style=for-the-badge&logo=react-router&logoColor=white)

## ✨ Features

### 🛍️ Shopping Experience
- **Product Catalog** - Browse through 20+ products from various categories
- **Real-time Cart Updates** - Instant add/remove functionality with visual feedback
- **Animated Badge Counter** - Live cart item count with bounce animation
- **Responsive Grid Layout** - Adapts seamlessly from mobile to desktop

### 🎨 User Interface
- **Modern Design** - Clean, intuitive interface with hover effects
- **Toast Notifications** - Real-time feedback for all cart actions
- **Loading States** - Elegant spinner during data fetching
- **Image Optimization** - High-quality product images with proper sizing

### 📱 Responsive Design
- **Mobile-First Approach** - Optimized for smartphones and tablets
- **Adaptive Grid** - Automatic column adjustment based on screen size
- **Touch-Friendly** - Large, easy-to-tap buttons and cards

### 🔔 Smart Notifications
- **React Hot Toast** - Beautiful, customizable toast messages
- **Action Feedback** - Success/error messages for every operation
- **Non-intrusive** - Auto-dismiss with smooth animations

## 🚀 Live Demo

**[View Live Application](#)** *(Add your deployment link here)*

## 📸 Screenshots

### Home Page
*Product grid with add-to-cart functionality*

### Cart Page
*Detailed cart view with checkout summary*

## 🛠️ Tech Stack

### Core Technologies
- **React 18.2.0** - Modern UI library with hooks
- **Redux Toolkit 1.9.7** - Simplified state management
- **React Router DOM 6.9.0** - Client-side routing

### Styling & UI
- **Tailwind CSS 3.2.7** - Utility-first CSS framework
- **PostCSS** - CSS processing
- **React Icons 4.12.0** - Icon library

### Utilities
- **React Hot Toast 2.4.0** - Toast notifications
- **FakeStore API** - Product data source

## 📦 Installation

### Prerequisites

- **Node.js** (v14 or higher)
- **npm** or **yarn**

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/shopping-cart.git
   cd shopping-cart
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   ```
   http://localhost:3000
   ```

## 📁 Project Structure

```
shopping-cart/
├── public/
│   ├── index.html
│   ├── logo.png
│   ├── favicon.ico
│   └── site.webmanifest
├── src/
│   ├── components/
│   │   ├── Navbar.jsx           # Navigation with cart badge
│   │   ├── Product.jsx          # Product card component
│   │   ├── CartItem.jsx         # Cart item with remove functionality
│   │   ├── Spinner.jsx          # Loading spinner
│   │   └── Spinner.css          # Spinner animations
│   ├── pages/
│   │   ├── Home.jsx             # Product listing page
│   │   └── Cart.jsx             # Shopping cart page
│   ├── redux/
│   │   ├── Store.js             # Redux store configuration
│   │   └── Slices/
│   │       └── CartSlice.js     # Cart state management
│   ├── data.js                  # Product data
│   ├── App.jsx                  # Main app component
│   ├── index.js                 # App entry point
│   └── index.css                # Global styles
├── .gitignore
├── package.json
├── tailwind.config.js
├── postcss.config.js
└── README.md
```

## 🎯 Key Features Explained

### State Management with Redux Toolkit

The app uses Redux Toolkit for efficient state management:

```javascript
// CartSlice.js - Simple, intuitive reducers
add: (state, action) => {
    state.push(action.payload);
},
remove: (state, action) => {
    return state.filter((item) => item.id !== action.payload);
}
```

### Real-time Cart Badge

Dynamic badge showing cart item count with animations:
- Bounces when items are added
- Auto-updates across all pages
- Shows count only when cart has items

### Smart Add/Remove Logic

Products intelligently toggle between "Add to Cart" and "Remove Item" based on current cart state:

```javascript
cart.some((p) => p.id == post.id) ? 
    <RemoveButton /> : <AddButton />
```

### Toast Notifications

User-friendly feedback for every action:
- ✅ Success toast on item addition
- ❌ Error toast on item removal
- Auto-dismiss with smooth animations

## 🔧 Available Scripts

### Development

```bash
npm start
```
Runs the app in development mode at [http://localhost:3000](http://localhost:3000)

### Build

```bash
npm run build
```
Creates an optimized production build in the `build/` folder

### Test

```bash
npm test
```
Launches the test runner in interactive watch mode




The app fetches product data from [FakeStore API](https://fakestoreapi.com/):

**Endpoint:** `https://fakestore
