# Real Estate Platform

A full-stack real estate website built with Next.js, Express, and PostgreSQL.

## 🏗️ Project Structure

```
real-estate-platform/
├── frontend/          # Next.js 14 React frontend
├── backend/           # Express.js API server
└── .github/           # Configuration files
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- Supabase account (https://supabase.com)
- npm or yarn

### Installation

1. **Setup Frontend**

   ```bash
   cd frontend
   npm install
   npm run dev
   ```

   Frontend runs on `http://localhost:3000`

2. **Setup Backend**

   ```bash
   cd backend
   npm install
   npm run dev
   ```

   API runs on `http://localhost:5000`

3. **Database Setup with Supabase**
   - Create account at https://supabase.com
   - Create a new project
   - Go to Settings > Database > Connection String
   - Copy the connection string and paste it in `/backend/.env` as `DATABASE_URL`
   - Database tables auto-migrate on server start

## 📚 Features

- **Property Listings**: Browse available properties
- **Property Details**: View detailed information about each property
- **REST API**: Full CRUD operations for properties
- **Responsive Design**: Mobile-friendly interface
- **Type-Safe**: TypeScript for both frontend and backend

## 🛠️ Tech Stack

- **Frontend**: Next.js 14, React 18, TypeScript, Axios
- **Backend**: Express.js, TypeScript, Sequelize ORM
- **Database**: PostgreSQL with Supabase
- **Styling**: CSS-in-JS (inline styles)

## 📝 API Endpoints

### Properties

- `GET /api/properties` - Get all properties
- `GET /api/properties/:id` - Get property by ID
- `POST /api/properties` - Create new property
- `PUT /api/properties/:id` - Update property
- `DELETE /api/properties/:id` - Delete property

## 🧪 Example API Request

```bash
# Get all properties
curl http://localhost:5000/api/properties

# Get specific property
curl http://localhost:5000/api/properties/1

# Create property
curl -X POST http://localhost:5000/api/properties \
  -H "Content-Type: application/json" \
  -d '{
    "title": "Modern Apartment",
    "price": 250000,
    "location": "Downtown",
    "beds": 2,
    "baths": 1,
    "description": "Beautiful modern apartment with great views"
  }'
```

## 📦 Scripts

### Frontend

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server

### Backend

- `npm run dev` - Start development server with auto-reload
- `npm run build` - Compile TypeScript
- `npm start` - Start production server

## 🔧 Configuration

### Frontend Environment Variables (`.env.local`)

```
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

### Backend Environment Variables (`.env`)

```
PORT=5000
NODE_ENV=development
DATABASE_URL=postgresql://[user]:[password]@[host]:[port]/[database]
```

**Get your Supabase connection string:**

1. Log in to https://app.supabase.com
2. Select your project
3. Go to Settings > Database > Connection String
4. Select "Pooler" mode (recommended for production)
5. Copy and paste the connection string into `.env` file

## 📄 License

MIT
