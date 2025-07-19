# Elevate Workforce Solutions - Job Portal

A comprehensive job portal web application built for Elevate Workforce Solutions to digitize their hiring processes and connect job seekers with employers across Nepal.

## 🚀 Features

### Authentication System
- Secure user registration and login
- JWT-based authentication
- Role-based access control (Job Seekers & Companies)
- Password hashing with bcrypt

### Job Management
- Browse job listings with pagination
- Advanced job search functionality
- Detailed job descriptions and requirements
- Company-specific job management dashboard

### Application System
- Job seekers can apply to jobs with cover letters
- Companies can view and manage applications
- Application status tracking (pending, reviewed, accepted, rejected)

### Company Dashboard
- Post, edit, and delete job listings
- View application statistics
- Manage job applications
- Company profile management

### User Experience
- Responsive design with Bootstrap 5
- Beautiful gradient backgrounds and modern UI
- Mobile-friendly interface
- Real-time notifications and feedback

## 🛠️ Technology Stack

- **Backend**: Node.js + Express.js
- **Frontend**: EJS Templates
- **Database**: MySQL
- **Authentication**: JWT (JSON Web Tokens)
- **Styling**: Bootstrap 5 + Custom CSS
- **Icons**: Font Awesome
- **Password Security**: bcryptjs

## 📋 Prerequisites

- Node.js (v14 or higher)
- MySQL (v8.0 or higher)
- npm or yarn package manager

## 🔧 Installation & Setup

1. **Clone the repository**
   \`\`\`bash
   git clone <repository-url>
   cd elevate-workforce-portal
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   \`\`\`

3. **Database Setup**
   - Create a MySQL database named `job_portal`
   - Run the SQL schema from `database/schema.sql`
   - Update database credentials in `.env` file

4. **Environment Configuration**
   Create a `.env` file in the root directory:
   \`\`\`env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_password
   DB_NAME=job_portal
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRES_IN=7d
   NODE_ENV=development
   PORT=3000
   \`\`\`

5. **Seed the Database (Optional)**
   \`\`\`bash
   node scripts/seed-database.js
   \`\`\`

6. **Start the Application**
   \`\`\`bash
   # Development mode
   npm run dev
   
   # Production mode
   npm start
   \`\`\`

7. **Access the Application**
   Open your browser and navigate to `http://localhost:3000`

## 🏗️ Project Structure

\`\`\`
elevate-workforce-portal/
├── config/
│   └── database.js          # Database configuration
├── controllers/
│   ├── AuthController.js    # Authentication logic
│   ├── JobController.js     # Job management logic
│   ├── CompanyController.js # Company dashboard logic
│   └── ApplicationController.js # Application management
├── middleware/
│   └── auth.js             # Authentication middleware
├── models/
│   ├── User.js             # User model (OOP)
│   ├── Job.js              # Job model (OOP)
│   └── Application.js      # Application model (OOP)
├── routes/
│   ├── authRoutes.js       # Authentication routes
│   ├── jobRoutes.js        # Job-related routes
│   ├── companyRoutes.js    # Company dashboard routes
│   └── applicationRoutes.js # Application routes
├── views/
│   ├── layout.ejs          # Main layout template
│   ├── auth/               # Authentication views
│   ├── jobs/               # Job listing views
│   ├── company/            # Company dashboard views
│   └── error.ejs           # Error page
├── database/
│   └── schema.sql          # Database schema
├── scripts/
│   └── seed-database.js    # Database seeding script
├── server.js               # Main application file
└── package.json            # Dependencies and scripts
\`\`\`

## 🎨 Design Features

- **Gradient Backgrounds**: Beautiful color gradients throughout the application
- **Modern Cards**: Clean card-based design with shadows and hover effects
- **Responsive Layout**: Mobile-first design that works on all devices
- **Color Scheme**: Professional blue, red, green, and yellow accents
- **Interactive Elements**: Smooth transitions and hover effects
- **Typography**: Clean, readable fonts with proper hierarchy

## 👥 User Roles

### Job Seekers
- Browse and search job listings
- View detailed job descriptions
- Apply to jobs with cover letters
- Track application status
- Manage profile information

### Companies
- Post new job listings
- Edit and delete existing jobs
- View and manage job applications
- Access dashboard with statistics
- Update company information

## 🔐 Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Protected routes with middleware
- Input validation and sanitization
- SQL injection prevention
- XSS protection

## 📱 API Endpoints

### Authentication
- `GET /auth/register` - Registration form
- `POST /auth/register` - Create new account
- `GET /auth/login` - Login form
- `POST /auth/login` - Authenticate user
- `GET /auth/logout` - Logout user

### Jobs
- `GET /jobs` - List all jobs with pagination
- `GET /jobs/:id` - View job details

### Company Dashboard
- `GET /company/dashboard` - Company dashboard
- `GET /company/jobs/create` - Job creation form
- `POST /company/jobs/create` - Create new job
- `GET /company/jobs/:id/edit` - Edit job form
- `POST /company/jobs/:id/edit` - Update job
- `DELETE /company/jobs/:id` - Delete job

### Applications
- `POST /applications/apply/:jobId` - Apply to job
- `GET /applications/my-applications` - View user's applications
- `PUT /applications/:id/status` - Update application status

## 🚀 Deployment

1. **Production Environment Variables**
   \`\`\`env
   NODE_ENV=production
   DB_HOST=your_production_db_host
   DB_USER=your_production_db_user
   DB_PASSWORD=your_production_db_password
   JWT_SECRET=your_strong_jwt_secret
   \`\`\`

2. **Database Migration**
   - Run the schema.sql on your production database
   - Ensure proper database permissions

3. **Start Production Server**
   \`\`\`bash
   npm start
   \`\`\`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Developer

Built with ❤️ for Elevate Workforce Solutions by Code Art Web Technologies

## 📞 Support

For support and queries, please contact:
- Email: info@elevateworkforce.com
- Phone: +977-1-4567890
- Address: Kathmandu, Nepal
