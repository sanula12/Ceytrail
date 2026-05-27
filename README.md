# CeyTrail 🚗🌴

A full-stack ride-hailing and tourism platform for Sri Lanka — connecting customers with drivers for taxi rides, multi-day travel bookings, and tour packages.

> **Live:** [ceytrail.com](https://ceytrail.com)

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 16 (App Router), React 19 |
| Language | TypeScript |
| Styling | Tailwind CSS v4, Material UI v7 |
| Database | MySQL + Prisma ORM v6 |
| Auth | Better Auth |
| Real-time | Ably WebSockets |
| Maps | Google Maps API |
| Payments | PayHere (Card + Tokenization) |
| Email | Resend |
| Deployment | Vercel + Docker |

---

## ✨ Key Features

### 🧑 Customer
- Book point-to-point taxi rides with live driver tracking
- **Split Rides (Carpooling)** — share a ride and split the fare
- Multi-day travel bookings with a **live driver bidding engine**
- Browse inbound/outbound tour packages with itineraries
- Submit inquiries for tours, flights, visas, and entertainment
- Pay via cash or card (PayHere integration)

### 🚗 Driver
- Real-time ride requests via Ably WebSockets
- Competitive bidding on customer travel requests
- Wallet system — track earnings, commissions, and payouts
- Upload and manage vehicle documents for admin approval
- Chauffeur profile support (SLTDA IDs for tourist driving)

### 🛠️ Admin
- Approve/suspend drivers, customers, and vehicle documents
- Monitor all platform transactions and financial movements
- Approve driver withdrawal requests and cash payment proofs
- Manage destinations, tour packages, pricing, and ride categories
- Dynamic pricing config — base price, per km rate, waiting charges

---

## 🗃️ Database Highlights

- **User** — unified table for Customers, Drivers, and Admins with wallet balances
- **Ride + RidePassenger** — supports both standard and split-ride carpooling
- **Bid** — stores driver bids on ride and travel booking requests
- **Transaction** — immutable financial ledger for all platform movements
- **Inquiry tables** — TourInquiry, VisaInquiry, TicketInquiry, EntertainmentInquiry

---

## 🚀 Getting Started

```bash
# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Sync database schema
npx prisma db push

# Seed initial data
npm run prisma:seed

# Start development server
npm run dev
```

---

## 📁 Project Structure

```
app/
├── (public)/       # Customer-facing frontend
├── driver/         # Driver dashboard
├── dashboard/      # Admin control panel
lib/
├── auth.ts         # Authentication config
├── ably.ts         # Real-time WebSocket setup
├── payhere.ts      # Payment gateway integration
├── prisma.ts       # Database client
components/         # Reusable UI components
prisma/
└── schema.prisma   # Full database schema
```

---

## 👨‍💻 Built By

**Sanula Kariyapperuma** — Sole developer  
[github.com/sanula12](https://github.com/sanula12) · [linkedin.com/in/sanula-kariyapperuma](https://linkedin.com/in/sanula-kariyapperuma)
