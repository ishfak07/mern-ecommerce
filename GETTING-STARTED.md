# 🚀 Quick Start Guide

## Prerequisites Checklist
- [ ] Node.js installed (v14+)
- [ ] MongoDB installed and running OR MongoDB Atlas account
- [ ] Git installed

## First Time Setup

### 1. Database Setup
Choose one of the following options:

#### Option A: Local MongoDB
```bash
# Start MongoDB service (Windows)
net start MongoDB

# Or if using MongoDB Community Edition
mongod
```

#### Option B: MongoDB Atlas (Cloud)
1. Go to https://www.mongodb.com/atlas
2. Create free account and cluster
3. Get connection string
4. Update MONGO_URI in server/.env

### 2. Environment Configuration
✅ Environment files are already created with default values.

**Important:** Update these values in `server/.env`:
- `JWT_SECRET` - Change to a secure random string
- `MONGO_URI` - Update if using MongoDB Atlas

### 3. Start the Application
```bash
# From project root directory
npm run dev
```

This will start:
- Backend server on http://localhost:3000
- Frontend development server on http://localhost:8080

### 4. Create Admin User
```bash
# In a new terminal, go to server directory
cd server
npm run seed:db your-email@example.com your-secure-password
```

## Available Scripts
- `npm run dev` - Start both client and server in development mode
- `npm run dev:client` - Start only client development server
- `npm run dev:server` - Start only server development server

## Troubleshooting

### Common Issues:

1. **MongoDB Connection Error**
   - Ensure MongoDB is running
   - Check MONGO_URI in server/.env

2. **Port Already in Use**
   - Kill processes on ports 3000 or 8080
   - Or change PORT in server/.env

3. **Dependencies Issues**
   - Delete node_modules folders
   - Run `npm install` in root directory

### Getting Help
- Check console errors in browser
- Check terminal output for backend errors
- Ensure all environment variables are set

## Next Steps
1. ✅ Project is cleaned and personalized
2. ✅ Dependencies installed
3. ✅ Environment files created
4. 🔄 Start the application
5. 🔄 Create admin user
6. 🔄 Begin development

**Happy Coding! 🎉**