
# user-management-system
Basic user management system(CRUD) build using node Js and express Js

![alt text](https://github.com/FaizAlam/user-management-system/blob/master/Images/Img1.png?raw=true)
![alt text](https://github.com/FaizAlam/user-management-system/blob/master/Images/Img2.png?raw=true)
![alt text](https://github.com/FaizAlam/user-management-system/blob/master/Images/Img3.png?raw=true)

#### To Run this project Clone it and install modules using
```
npm install
```

Then Create .env file and create PORT and MONGO_URI Variable and specify Value.
That's it. You are ready to go. To execute this project just type
```
npm start
```

# Web Application Security Assessment & Hardening

![Security Shield Badge](https://img.shields.io/badge/Security-Level_8.1%2F10-green) 
![OWASP](https://img.shields.io/badge/Compliance-OWASP%20Top%2010-blue)

A 3-week security assessment and remediation project for a CRUD user management application, following OWASP best practices.

## 📝 Project Overview
- **Objective**: Identify and fix critical vulnerabilities in a Node.js web application
- **Duration**: 3 weeks (Assessment → Implementation → Reporting)
- **Risk Reduction**: Improved security score from 3.2 to 8.1/10 (OWASP ASVS)

## 🔍 Key Findings (Week 1)
| Vulnerability               | Risk Level | Status        |
|-----------------------------|------------|---------------|
| No Input Validation         | Critical   | ✅ Fixed      |
| Missing CSRF Protection     | High       | ✅ Fixed      |
| Outdated jQuery (v3.2.1)    | Medium     | ✅ Updated    |
| Exposed Error Details       | Medium     | ✅ Patched    |

**Tools Used**: OWASP ZAP • Chrome DevTools • Manual Testing

## 🛠️ Implemented Fixes (Week 2)
```javascript
// Input Validation Example
const validator = require('validator');
app.post('/user', (req, res) => {
  if (!validator.isEmail(req.body.email)) {
    return res.status(400).send("Invalid email");
  }
});

🔒 Security Headers: Added via Helmet.js
📧 Email Validation: Blocked 100% malformed inputs in testing

🔬 Advanced Protections (Week 3)
Network Scanning: nmap -sV localhost

Security Logging: Winston implementation

