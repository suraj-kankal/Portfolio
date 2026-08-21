# 💼 Suraj Kankal - Portfolio

A full-stack portfolio website showcasing my skills as a **Full Stack Java Developer**.

## 🚀 Live Demo

- **Frontend:** [Portfolio Website](https://suraj-kankal.github.io/Portfolio)
- **Backend API:** [http://localhost:3000](http://localhost:3000)
- **API Documentation:** See endpoints below

---

## 📱 Features

✅ **Dynamic Portfolio Data** - Fetched from backend API  
✅ **Contact Form** - Submissions saved to SQLite database  
✅ **Admin Dashboard** - View and manage contacts  
✅ **Responsive Design** - Works on all devices  
✅ **Smooth Animations** - Scroll effects and transitions  
✅ **Token Authentication** - Protected admin endpoints  
✅ **API-First Architecture** - Clean separation of frontend/backend  

---

## 🛠️ Tech Stack

### **Frontend**
- HTML5
- CSS3 
- JavaScript 
- Font Awesome Icons
- Google Fonts

### **Backend**
- Node.js
- Express.js
- SQLite3 (Database)
- CORS Enabled
- JWT Authentication (Bearer Tokens)

### **Tools & Services**
- Git / GitHub
- VS Code
- Postman (API Testing)
- NPM (Package Manager)

---

## 📁 Project Structure

```
Portfolio/
├── Portfolio.html          # Frontend - Main page
├── server.js               # Backend - Express server
├── database.js             # Database - SQLite operations
├── view-database.js        # Utility - View database
├── portfolio.db            # SQLite Database (auto-created)
├── environment.env         # Environment variables
├── package.json            # Dependencies
├── .gitignore              # Git ignore rules
│
└── Postman Collections/
    ├── Portfolio-API.postman_collection.json
    └── Portfolio-API-Database.postman_collection.json
```

---

## 🚀 Getting Started

### **Prerequisites**
- Node.js (v16+)
- Git
- Postman (for testing)

### **Installation**

1. **Clone Repository**
```bash
git clone https://github.com/suraj-kankal/Portfolio.git
cd Portfolio
```

2. **Install Dependencies**
```bash
npm install
```

3. **Setup Environment**
```bash
# Copy environment.env and update if needed
copy environment.env .env
```

4. **Start Backend Server**
```bash
node server.js
```

5. **Open Frontend**
```bash
# Open in browser
start Portfolio.html
# Or open http://localhost:3000 for API
```

---

## 📡 API Endpoints

### **Public Endpoints** (No Authentication)

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/` | Server status |
| `GET` | `/api/portfolio` | All portfolio data |
| `GET` | `/api/skills` | Skills only |
| `GET` | `/api/experience` | Experience only |
| `GET` | `/api/education` | Education only |
| `POST` | `/api/contact` | Submit contact form |

### **Protected Endpoints** (Requires Auth Token)

Header: `Authorization: Bearer admin_token_12345`

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/private-data` | Private data (admin) |
| `GET` | `/api/admin/contacts` | View all contacts |
| `GET` | `/api/admin/contacts/new` | View new contacts |
| `GET` | `/api/admin/contacts/:id` | View specific contact |
| `PUT` | `/api/admin/contacts/:id/status` | Update contact status |
| `DELETE` | `/api/admin/contacts/:id` | Delete contact |
| `GET` | `/api/admin/stats` | View statistics |

---

## 💾 Database Schema

### **contact_submissions Table**
```sql
CREATE TABLE contact_submissions (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  email TEXT NOT NULL,
  subject TEXT,
  message TEXT NOT NULL,
  ip_address TEXT,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  status TEXT DEFAULT 'new'
);
```

---

## 🧪 Testing with Postman

1. **Import Collections:**
   - `Portfolio-API-Database.postman_collection.json`

2. **Test Public Endpoints:**
   - `GET /api/portfolio`
   - `POST /api/contact`

3. **Test Protected Endpoints:**
   - Add header: `Authorization: Bearer admin_token_12345`
   - `GET /api/admin/contacts`

---

## 📊 View Database

### **Option 1: Node.js Script**
```bash
node view-database.js
```

### **Option 2: DB Browser**
1. Download [SQLite Browser](https://sqlitebrowser.org/)
2. Open `portfolio.db`
3. View tables and data visually

### **Option 3: SQLite CLI**
```bash
sqlite3 portfolio.db
SELECT * FROM contact_submissions;
```

---

## 🔐 Security Features

✅ **Token-Based Authentication** - Bearer token for admin endpoints  
✅ **CORS Enabled** - Controlled cross-origin requests  
✅ **Environment Variables** - Sensitive data in .env (not committed)  
✅ **Database Encryption** - IP tracking and timestamps  
✅ **Input Validation** - Backend validation for all inputs  

---

## 🌐 Deployment Options

### **Frontend (GitHub Pages)**
```bash
# Push to GitHub
git add .
git commit -m "Initial commit"
git push -u origin main

# Enable GitHub Pages in Settings → Pages
# Select "main" branch → Save
# Your site: https://suraj-kankal.github.io/Portfolio
```

### **Backend (Heroku)**
```bash
# Install Heroku CLI
choco install heroku-cli

# Login to Heroku
heroku login

# Create app
heroku create suraj-portfolio-api

# Push code
git push heroku main

# Your API: https://suraj-portfolio-api.herokuapp.com
```

### **Backend (Render.com)**
1. Go to [Render.com](https://render.com)
2. Connect GitHub
3. Select repository
4. Deploy
5. Set environment variables

---

## 📝 Skills Showcased

### **Backend**
- ✅ Express.js REST API
- ✅ SQLite Database Design
- ✅ Authentication & Authorization
- ✅ CORS Configuration
- ✅ Error Handling
- ✅ Environment Variables

### **Frontend**
- ✅ Async/Await Fetch API
- ✅ DOM Manipulation
- ✅ CSS Animations
- ✅ Responsive Design
- ✅ Form Validation
- ✅ API Integration

### **DevOps**
- ✅ Git/GitHub
- ✅ NPM Package Management
- ✅ Database Management
- ✅ API Testing (Postman)
- ✅ Deployment

---

## 📞 Contact & Links

- **Email:** surajkankal0606@gmail.com
- **GitHub:** https://github.com/suraj-kankal
- **LinkedIn:** https://www.linkedin.com/in/surajkankal
- **Portfolio:** https://suraj-kankal.github.io/Portfolio

---

## 📚 Learning Resources

- [Express.js Docs](https://expressjs.com)
- [SQLite Docs](https://www.sqlite.org/docs.html)
- [GitHub Pages Guide](https://pages.github.com)
- [Heroku Deployment](https://devcenter.heroku.com)

---

## 📄 License

This project is open source and available for personal and educational use.

---

## 🎯 Future Enhancements

- [ ] Add projects showcase section
- [ ] Implement email notifications
- [ ] Add admin dashboard UI
- [ ] Deploy to cloud (Heroku/Render)
- [ ] Add MongoDB support
- [ ] Implement caching
- [ ] Add analytics tracking
- [ ] Create Spring Boot version

---

**Built with ❤️ by Suraj Kankal**
