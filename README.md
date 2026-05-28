# Grocery Delivery Fullstack Application

A modern, full-featured e-commerce grocery delivery platform with real-time order tracking, secure authentication, and robust admin controls. Built for scalability, maintainability, and a seamless user experience.

---

## Features

### 🛒 Customer-Facing (Frontend)
- **Browse & Search Products:** Intuitive product catalog, categories, and search functionality
- **Cart & Checkout:** Add to cart, address management, secure checkout, and payment integration
- **Order Tracking:** Real-time order status, live map tracking, and OTP verification for delivery
- **Flash Deals & Promotions:** Highlighted deals, banners, and newsletter subscriptions
- **Authentication:** Secure login, registration, and protected routes

### 🚚 Delivery Partner Portal
- **Order Management:** View assigned deliveries, update status, OTP verification for handoff
- **Live Tracking:** Integrated map for delivery routes

### 🛠️ Admin Dashboard
- **Product Management:** Add, edit, or remove products with image uploads (Cloudinary integration)
- **Order Oversight:** Monitor all orders, update statuses, and manage delivery assignments
- **Delivery Partner Management:** Add or remove partners, assign orders
- **Analytics & Controls:** Dashboard for key metrics and system controls

---

## Tech Stack

### Frontend
- **React + TypeScript** (Vite)
- **Context API** for state management
- **Modern UI/UX** with responsive design

### Backend
- **Node.js + Express**
- **Prisma ORM** (with PostgreSQL or other supported DB)
- **Cloudinary** for image uploads
- **Nodemailer** for transactional emails
- **Vercel** for deployment

### Other Integrations
- **Real-time features** (order tracking, OTP)
- **Secure authentication** (JWT or similar)

---

## Project Structure

```
client/           # Frontend React app
  src/
    components/   # Reusable UI components
    pages/        # Route-based pages (Home, Products, Checkout, Admin, etc.)
    context/      # Auth & Cart context providers
    config/       # API configs
    types/        # TypeScript types
server/           # Backend Node.js app
  controllers/    # Route controllers (auth, orders, products, etc.)
  routes/         # Express routes
  config/         # Service configs (Cloudinary, Prisma, etc.)
  prisma/         # Prisma schema
  inngest/        # Event-driven logic
  types/          # TypeScript types
```

---

## Getting Started

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Dev-Champions-Projects/grocery_delivery.git
   ```
2. **Install dependencies:**
   - Frontend: `cd client && npm install`
   - Backend: `cd server && npm install`
3. **Configure environment variables:**
   - Create a `.env` file in both `client` and `server` directories. Use the following pattern for the server:

     ```env
     # JWT Secret
     JWT_SECRET="your_jwt_secret"

     # Can Add Multiple Admins By Adding Commas
     ADMIN_EMAILS="admin@example.com"

     # Neon Database (postgres)
     DATABASE_URL="your_postgres_connection_url"

     # Cloudinary
     CLOUDINARY_CLOUD_NAME="your_cloud_name"
     CLOUDINARY_API_KEY="your_api_key"
     CLOUDINARY_API_SECRET="your_api_secret"

     # Inngest
     INNGEST_EVENT_KEY="your_inngest_event_key"
     INNGEST_SIGNING_KEY="your_inngest_signing_key"

     # SMTP Credentials
     SENDER_EMAIL="your_sender_email"
     SMTP_USER="your_smtp_user"
     SMTP_PASS="your_smtp_pass"

     # Stripe Credentials
     STRIPE_SECRET_KEY="your_stripe_secret_key"
     STRIPE_WEBHOOK_SECRET="your_stripe_webhook_secret"

     CLIENT_URL="http://localhost:5173"
     ```

     > **Note:** Never commit your real `.env` file or secrets to version control.
4. **Run locally:**
   - Backend: `npm run dev` (from `server`)
   - Frontend: `npm run dev` (from `client`)
5. **Database setup:**
   - Configure your database in `server/prisma/schema.prisma` and run migrations

---

## Future-Proofing & Notes

- **Modular structure** for easy feature expansion
- **TypeScript everywhere** for maintainability
- **Environment-based configs** for deployment flexibility
- **Admin and Delivery roles** are extensible for future needs
- **Cloud services** (Cloudinary, Vercel) can be swapped as needed

---

## License

This project is for educational and portfolio purposes. For commercial use, please contact the author.

---

## Author

- [Dev Champions Projects](https://github.com/Dev-Champions-Projects)

---

> _"Build with scalability and future you in mind!"_
