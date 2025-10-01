# MERN E-commerce Store

## Description

A modern, full-featured e-commerce store built with the MERN stack (MongoDB, Express.js, React, Node.js) and integrated with third-party APIs. This application supports three main user flows:

1. **Buyers** - Browse store categories, products, and brands
2. **Sellers/Merchants** - Manage their own brand components and products
3. **Admins** - Complete control and management of the entire store

### 🚀 Key Features:

* **Backend**: Node.js with Express.js for robust server-side functionality
* **Database**: MongoDB with Mongoose for efficient data modeling
* **Frontend**: React with Redux for state management
* **Authentication**: JWT-based authentication with social login options
* **File Upload**: AWS S3 integration for image storage
* **Email Services**: Mailgun integration for transactional emails
* **Newsletter**: Mailchimp integration for marketing campaigns
* **Real-time Features**: Socket.io for live customer support
* **Responsive Design**: Mobile-first approach with Bootstrap
* **Payment Integration**: Ready for payment gateway integration

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- Git

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/ishfak07/mern-ecommerce.git
cd mern-ecommerce
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up environment variables**
   - Copy `.env.example` files in both client and server directories
   - Rename them to `.env` and configure with your settings

4. **Start development servers**
```bash
npm run dev
```

The application will be available at:
- Frontend: http://localhost:8080
- Backend API: http://localhost:3000

## Database Seed

* The seed command will create an admin user in the database
* The email and password are passed with the command as arguments
* Like below command, replace brackets with email and password. 
* For more information, see code [here](server/utils/seed.js)

```
npm run seed:db [email-***@****.com] [password-******] // This is just an example.
```

## Install

`npm install` in the project root will install dependencies in both `client` and `server`. [See package.json](package.json)

Some basic Git commands are:

```
git clone https://github.com/mohamedsamara/mern-ecommerce.git
cd project
npm install
```

## 📋 Environment Variables

### Client (.env)
Create a `.env` file in the `client` directory:
```bash
API_URL=http://localhost:3000/api
```

### Server (.env)
Create a `.env` file in the `server` directory with the following variables:
```bash
PORT=3000
MONGO_URI=mongodb://127.0.0.1:27017/mern_ecommerce
JWT_SECRET=your_jwt_secret_key_here

# Email Services (Optional)
MAILCHIMP_KEY=your_mailchimp_key
MAILCHIMP_LIST_KEY=your_mailchimp_list_key
MAILGUN_KEY=your_mailgun_key
MAILGUN_DOMAIN=your_mailgun_domain
MAILGUN_EMAIL_SENDER=your_email@domain.com

# Social Authentication (Optional)
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:3000/api/auth/google/callback
FACEBOOK_CLIENT_ID=your_facebook_client_id
FACEBOOK_CLIENT_SECRET=your_facebook_client_secret
FACEBOOK_CALLBACK_URL=http://localhost:3000/api/auth/facebook/callback

# Frontend URL
CLIENT_URL=http://localhost:8080
BASE_API_URL=api

# AWS S3 (Optional - for file uploads)
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=us-east-2
AWS_BUCKET_NAME=your_bucket_name
```

## 🗄️ Database Setup

### Option 1: Using MongoDB Locally
1. Install MongoDB on your system
2. Start MongoDB service
3. The application will connect to `mongodb://127.0.0.1:27017/mern_ecommerce`

### Option 2: Using MongoDB Atlas (Cloud)
1. Create a free account at [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create a new cluster
3. Get your connection string
4. Update `MONGO_URI` in your server `.env` file

### Database Seeding
Create an admin user and sample data:
```bash
cd server
npm run seed:db your-email@example.com your-password
```

## 🐳 Docker Setup (Alternative)

If you prefer using Docker:

1. **Update docker-compose.yml**
   - Set your `MONGO_URI` and `JWT_SECRET` values

2. **Build and run**
```bash
docker-compose build
docker-compose up
```

## 🚀 Deployment

### Vercel Deployment
This project is configured for Vercel deployment:

1. **Frontend Deployment**
   - Root directory: `client`
   - Build command: `npm run build`
   - Output directory: `dist`

2. **Backend Deployment**
   - Root directory: `server`
   - Build command: `npm install`
   - Output directory: `./`

## 🛠️ Development Tools

### VS Code Setup
For better development experience:

1. Create `.vscode/settings.json`:
```json
{
  "editor.formatOnSave": true,
  "prettier.singleQuote": true,
  "prettier.arrowParens": "avoid",
  "prettier.jsxSingleQuote": true,
  "prettier.trailingComma": "none",
  "javascript.preferences.quoteStyle": "single"
}
```

2. Install recommended extensions:
   - Prettier - Code formatter
   - ES7+ React/Redux/React-Native snippets
   - Auto Rename Tag
   - Bracket Pair Colorizer

## 📦 Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **Passport.js** - Social authentication
- **Multer** - File uploads
- **Socket.io** - Real-time communication

### Frontend
- **React** - UI library
- **Redux** - State management
- **React Router** - Navigation
- **Bootstrap** - CSS framework
- **Axios** - HTTP client
- **Webpack** - Module bundler

### Third-party Integrations
- **AWS S3** - File storage
- **Mailgun** - Email service
- **Mailchimp** - Newsletter management
- **Google/Facebook** - Social authentication

## 📱 Features

### For Customers
- Browse products by categories and brands
- Search and filter products
- Add products to cart and wishlist
- User registration and authentication
- Social login (Google, Facebook)
- Order management
- Product reviews and ratings

### For Merchants
- Merchant registration and management
- Add and manage products
- Brand management
- Order tracking
- Sales analytics

### For Administrators
- Complete store management
- User and merchant management
- Category and brand management
- Order management
- Analytics dashboard

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Original project inspiration from the MERN stack community
- Bootstrap for responsive design components
- All the amazing open-source libraries used in this project

## 📞 Support

If you have any questions or need help getting started, please:
- Open an issue in this repository
- Check the existing documentation
- Review the code comments for implementation details

---

**Happy Coding! 🚀**

