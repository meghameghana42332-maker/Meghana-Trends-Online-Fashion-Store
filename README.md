# 🛍️ B.K. MEGHANA SHOPPING MALL
### E-Commerce Web Application & QA Software Test Automation Project

[![Test Suite](https://img.shields.io/badge/Test%20Suite-42%20Tests%20Passed-brightgreen)](testing/test-reports/test_execution_summary.md)
[![Automation](https://img.shields.io/badge/Automation-Playwright%20%7C%20Selenium-blue)](#-automation-testing)
[![Tech Stack](https://img.shields.io/badge/Stack-HTML5%20%7C%20CSS3%20%7C%20JS%20%7C%20Node.js-orange)](#-technology-stack)
[![Role](https://img.shields.io/badge/Role-QA%20%2F%20Test%20Engineer-purple)](#-project-overview)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 Project Overview

**B.K. MEGHANA SHOPPING MALL** is an online fashion e-commerce web application and QA test automation project developed and maintained by **B.K. MEGHANA**. 

Designed as a showcase for **Software Test Engineer / QA roles**, this repository demonstrates expertise across three core competencies:
1. **Web Development**: Realistic e-commerce storefront with Men, Women, Kids, Offers, Coupons, Demo Gold & Silver Coins, Shopping Cart, Wishlist, Multi-step Checkout, Order Tracking, and an Admin Dashboard.
2. **Software Testing**: Industry-standard QA artifacts including Master Test Scenarios, 42 Manual Test Cases (CSV), Boundary Value Analysis, Negative Testing, Bug Reports with RCA, and Test Execution Summaries.
3. **Test Automation**: Cross-browser End-to-End automated test suites implemented in **Playwright (JavaScript)** and **Selenium WebDriver (Python with Page Object Model)** using stable `data-testid` selectors.

---

## 🌟 Key Application Features

| Module | Features & Capabilities |
| :--- | :--- |
| **🏠 Storefront & Branding** | Luxury responsive fashion UI, announcement bar, hero banner carousel, quick category banners, trust badges. |
| **👨 Men's Apparel** | Shirts, T-Shirts, Jeans, Trousers, Quilted Biker Jackets, Royal Silk Kurta Sets. |
| **👩 Women's Collection** | Pure Kanjivaram Silk Sarees, Handcrafted Designer Anarkalis, Bridal Velvet Lehengas, Georgette Dresses, High-Rise Jeans. |
| **👶 Kids & Baby Wear** | Boys' Cotton Sets, Girls' Party Frocks, Baby Organic Rompers, Festive Nehru Jacket Sets. |
| **🪙 Gold Coins (Demo)** | 24K 999 Purity Demo Gold Coins (1g, 2g, 5g, 10g) with certicard specifications. |
| **🥈 Silver Coins (Demo)** | 999 Fine Pure Demo Silver Coins (1g, 5g, 10g, 20g) with Lakshmi & Om motifs. |
| **🔍 Search & Multi-Filters** | Real-time search with live dropdown suggestions, category filters, subcategory checkboxes, price range slider (₹199 - ₹100,000), customer rating filters, and 6 sorting algorithms. |
| **🛒 Cart & Coupon Engine** | Slide-out cart drawer, dynamic badge count, quantity controls (1-10 with boundary protection), free shipping progress bar (threshold ₹999), and coupon discount calculator (`MEGHANA10`, `NEWUSER200`, `FESTIVE20`, `KIDS15`, `MEGA500`). |
| **❤️ Wishlist** | 1-Click persistent wishlist toggle, heart animations, dedicated wishlist view with "Move to Cart". |
| **💳 Multi-Step Checkout** | Step 1: Address validation (Full name, 10-digit mobile, 6-digit pincode), Step 2: Delivery speed, Step 3: Simulated Payment (Demo UPI, Demo Card, COD), Step 4: Order Confirmation with unique ID (`BKM-XXXXX`). |
| **📦 Order Tracking** | Visual order lifecycle timeline (Ordered → Confirmed → Packed → Shipped → Delivered). |
| **⚙️ Admin Dashboard** | Live KPI metrics (Total Products, Users, Orders, Revenue), Product Inventory CRUD (Add / Delete), Order status controller, and Coupon list. |
| **👤 Authentication** | Form validations, registration, login session persistence in `localStorage`. |

---

## 🏗️ Project Architecture

```
ONLINE PROJECT/
├── index.html                           # Main storefront application (instant browser launch)
├── admin.html                           # Admin Dashboard (KPIs, catalog CRUD, order status)
├── css/
│   ├── style.css                        # Theme variables, typography, responsive layout
│   ├── components.css                   # Modals, cart drawer, toast notifications, badges
│   └── admin.css                        # Admin dashboard layout, tables, KPI widgets
├── js/
│   ├── data.js                          # Master catalog data (Products, Categories, Coupons, Offers)
│   ├── app.js                           # Storefront controller, search, filters, sorting, modals
│   ├── cart.js                          # Cart calculations, quantity limits, coupon engine
│   ├── wishlist.js                      # Persistent wishlist operations
│   ├── orders.js                        # Multi-step checkout submission & order lifecycle
│   ├── auth.js                          # User registration, login, test accounts
│   ├── checkout.js                      # Checkout multi-step flow & validation logic
│   └── admin.js                         # Admin metrics, CRUD products, order status updater
├── backend/
│   ├── server.js                        # Node.js + Express REST API server
│   └── package.json                     # Server dependencies
├── database/
│   ├── schema.sql                       # Relational schema (MySQL / PostgreSQL)
│   ├── seed_data.sql                    # Initial seed data for products, users, coupons
│   └── db_structure.md                  # Entity Relationship (ER) & SQL interview queries
├── testing/
│   ├── test-scenarios.md                # Comprehensive QA Test Scenarios across 9 modules
│   ├── test-cases/
│   │   ├── TC_Registration_Login.csv    # 10 test cases (Auth module)
│   │   ├── TC_Product_Search_Filter.csv # 16 test cases (Search, Navigation, Filters)
│   │   ├── TC_Cart_Coupons.csv          # 15 test cases (Cart calculations, Coupons)
│   │   ├── TC_Checkout_Orders.csv       # 10 test cases (Checkout validations, Orders)
│   │   └── TC_Admin_Dashboard.csv       # 6 test cases (Admin KPIs, CRUD, Status updates)
│   ├── bug-reports/
│   │   ├── BUG-TEMPLATE.md              # Industry standard Bug Report template
│   │   ├── BUG-001-NegativeQuantityCart.md
│   │   └── BUG-002-ExpiredCouponBypass.md
│   ├── test-data/
│   │   └── test_users_coupons.json      # Test datasets for boundary and positive/negative tests
│   └── test-reports/
│       └── test_execution_summary.md    # Summary of test execution results and QA sign-off
├── automation/
│   ├── playwright/                      # Playwright E2E Test Suite
│   │   ├── package.json
│   │   ├── playwright.config.js
│   │   └── tests/
│   │       ├── e2e_shopping.spec.js     # Complete user shopping journey
│   │       ├── search_filter.spec.js    # Search and multi-criteria filters
│   │       ├── cart_coupons.spec.js     # Cart calculations and promo coupons
│   │       └── auth_validation.spec.js  # Registration and login validations
│   └── selenium/                        # Selenium WebDriver Test Suite (Python + POM)
│       ├── requirements.txt
│       ├── conftest.py                  # Pytest browser fixtures
│       ├── pages/
│       │   ├── base_page.py
│       │   ├── home_page.py
│       │   ├── cart_page.py
│       │   └── checkout_page.py
│       └── tests/
│           ├── test_e2e_flow.py         # Full end-to-end checkout test
│           └── test_cart_operations.py  # Cart and coupon discount tests
├── .gitignore
├── LICENSE                              # MIT License
└── README.md                            # Portfolio documentation
```

---

## 🚀 Quick Start & How to Run

### Method 1: Instant Browser Launch (Zero Installation)
Simply open `index.html` in any modern web browser (Chrome, Edge, Firefox, Safari):
- **Storefront**: Double-click `index.html`
- **Admin Portal**: Double-click `admin.html`

All cart, wishlist, orders, and authentication states persist seamlessly in browser `localStorage`.

### Method 2: Run with Node.js Express Backend
```bash
# 1. Navigate to backend directory
cd backend

# 2. Install dependencies
npm install

# 3. Start the server
npm start

# 4. Open in browser
# http://localhost:5000
```

---

## 🧪 QA & Software Testing Artifacts

This repository includes a production-grade testing suite designed to showcase end-to-end QA methodologies:

### 1. Test Scenarios (`testing/test-scenarios.md`)
High-level mapping covering 9 functional modules:
- User Registration & Authentication (`TS_AUTH`)
- Catalog Navigation & Subcategories (`TS_CATALOG`)
- Product Search & Live Autocomplete (`TS_SEARCH`)
- Product Details & Pincode Checker (`TS_DETAILS`)
- Cart Engine & Free Delivery Calculation (`TS_CART`)
- Coupon Application & Auto-Detach Logic (`TS_COUPON`)
- Multi-Step Checkout & Field Validations (`TS_CHECKOUT`)
- Wishlist Persistence & Transfer (`TS_WISHLIST`)
- Admin Dashboard Metrics & Inventory (`TS_ADMIN`)

### 2. Manual Test Cases (CSV)
- [TC_Registration_Login.csv](testing/test-cases/TC_Registration_Login.csv)
- [TC_Product_Search_Filter.csv](testing/test-cases/TC_Product_Search_Filter.csv)
- [TC_Cart_Coupons.csv](testing/test-cases/TC_Cart_Coupons.csv)
- [TC_Checkout_Orders.csv](testing/test-cases/TC_Checkout_Orders.csv)
- [TC_Admin_Dashboard.csv](testing/test-cases/TC_Admin_Dashboard.csv)

### 3. Defect Reports Logged & Resolved
- [BUG-001](testing/bug-reports/BUG-001-NegativeQuantityCart.md): Cart permitted negative or zero quantity upon manual DOM edit. *Fixed by enforcing boundary protection in `Cart.updateQuantity`.*
- [BUG-002](testing/bug-reports/BUG-002-ExpiredCouponBypass.md): Coupon discount remained applied after cart total dropped below minimum order requirement. *Fixed by real-time validation in `Cart.getTotals`.*

---

## 🤖 Automation Testing

All UI elements are instrumented with stable `data-testid` attributes (e.g. `data-testid="search-input"`, `data-testid="add-to-cart"`, `data-testid="apply-coupon"`), ensuring robust, flake-free automation.

### 1. Playwright Automation (JavaScript)
```bash
# Navigate to playwright folder
cd automation/playwright

# Install dependencies and browsers
npm install
npx playwright install chromium

# Run all automated tests
npm test

# Run tests in headed browser mode
npm run test:headed

# View HTML Test Report
npm run test:report
```

### 2. Selenium WebDriver Automation (Python + Pytest + POM)
```bash
# Navigate to selenium folder
cd automation/selenium

# Install requirements
pip install -r requirements.txt

# Run all test suites with HTML report output
pytest --html=reports/selenium_report.html --self-contained-html
```

---

## 🎟️ Demo Credentials & Test Coupons

### Test User Accounts
| Role | Email | Password |
| :--- | :--- | :--- |
| **Admin / Store Owner** | `meghana@bkmeghanafashion.com` | `Password123` |
| **QA Test Engineer** | `tester@bkmeghana.com` | `Password123` |

### Active Discount Coupons
| Coupon Code | Discount | Minimum Cart Value | Applicable Categories |
| :--- | :--- | :--- | :--- |
| `MEGHANA10` | 10% OFF | ₹999 | All Products |
| `NEWUSER200` | ₹200 FLAT | ₹500 | All Products |
| `FESTIVE20` | 20% OFF | ₹1,999 | All Products |
| `KIDS15` | 15% OFF | ₹799 | Kids Apparel |
| `MEGA500` | ₹500 FLAT | ₹3,999 | Premium Orders |

---

## 💻 Technology Stack

- **Frontend**: HTML5, CSS3 (Modern Flexbox & CSS Grid, Custom Design Variables), Vanilla JavaScript (ES6+ Modular Architecture).
- **Backend API**: Node.js, Express.js, CORS.
- **Database**: Relational Schema (MySQL 8.0+ / PostgreSQL 14+ compatible).
- **QA & Testing**: Manual Test Case Design, Boundary Value Analysis (BVA), Equivalence Class Partitioning (ECP).
- **Automation**: Playwright, Selenium WebDriver (Python), Pytest, Page Object Model (POM).

---

## 👤 Author & Project Owner

- **Project Owner:** **B.K. MEGHANA**
- **Target Role:** Test Engineer / QA Engineer
- **GitHub Repository:** [Meghana-Trends-Online-Fashion-Store](https://github.com/meghameghana42332-maker/Meghana-Trends-Online-Fashion-Store.git)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — free for educational, testing, and portfolio use.
