# 🛍️ Clothing Store App

An e-commerce platform for clothing that features separate admin and customer frontends. Customers can browse, add items to their cart, and complete purchases via WhatsApp. Admins can manage products, categories, and view order history.

---

## 📁 Project Structure

```

store/
├── clothing-store-frontend/   # React frontend for admin & customers
└── clothing-store-backend/    # Node.js + Express backend

````

---

## 🚀 Features

### 👨‍💼 Admin
- Admin login (protected)
- Upload/manage clothing products
- Create/edit/delete product categories
- Manage prices and availability
- View order history (from WhatsApp-based orders)

### 👤 Customer
- Browse products by category
- Product search and filter
- View product details
- Add items to cart
- WhatsApp-based checkout (no payment API integration)

---

## 💻 Frontend

### Tech Stack
- React.js
- Context API (Cart & Auth)
- Custom Hooks
- Styled with CSS (split by admin/common/customer)

### Key Paths
- `src/components/admin/`: Admin forms and dashboards
- `src/components/customer/`: Customer shopping experience
- `src/pages/`: Routing views
- `src/services/`: API handlers for products, categories, cart
- `src/utils/whatsappUtils.js`: Builds WhatsApp checkout message

### Run Frontend
```bash
cd clothing-store-frontend
npm install
npm start
````

---

## 🧠 Backend

### Tech Stack

* Node.js
* Express.js
* MongoDB (via Mongoose)
* Cloudinary (image uploads)
* RESTful API

### API Routes

* `/api/products` - manage products
* `/api/categories` - manage categories
* `/api/orders` - track orders
* `/api/admin` - admin login/auth

### Run Backend

```bash
cd clothing-store-backend
npm install
npm run dev
```

> ⚙️ Add `.env` file in the `clothing-store-backend` with:

```
PORT=5000
MONGO_URI=your_mongo_db_connection
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_key
CLOUDINARY_API_SECRET=your_secret
JWT_SECRET=your_jwt_secret
```

---

## 🛒 WhatsApp Checkout

Instead of integrating M-Pesa or card payments, the checkout button redirects the customer to WhatsApp with a **pre-filled order message** like:

```
Hello, I'd like to order:
- 2x Red Hoodie (Size M) - Ksh 3000
- 1x Blue Jeans (Size L) - Ksh 2000

Total: Ksh 5000
Name: John Doe
Address: Nairobi CBD
```

> Configurable in: `utils/whatsappUtils.js`

---

## 🛠️ To Do / Improvements

* [ ] Protect admin routes (JWT-based auth)
* [ ] Add pagination or lazy loading for large product sets
* [ ] Improve mobile responsiveness
* [ ] Add order logging in backend
* [ ] Add customer wishlists (optional)

---

## 📦 Deployment

### Frontend

* Deploy to [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/)

### Backend

* Deploy to [Render](https://render.com/), [Railway](https://railway.app/), or [Replit](https://replit.com/)

---

## 📄 License

MIT License. Free for personal and commercial use.