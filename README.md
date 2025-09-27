# 🎓 ITIans Platform  

منصة لخريجي معهد تكنولوجيا المعلومات (ITI) للتواصل مع الشركات، متابعة الوظائف، وتقديم الشكاوي.  
تم بناء المشروع باستخدام **Laravel (Backend) + React (Frontend) + PostgreSQL (Database) + Sanctum (Authentication).**

---

## 🛠 Tech Stack
- **Frontend:** React.js, TailwindCSS, react-i18next (Multi-language support)  
- **Backend:** Laravel 10, Sanctum Authentication  
- **Database:** PostgreSQL  
- **Testing:** PHPUnit, Manual Testing  
- **Version Control:** Git/GitHub  

---

## ✨ Features
- 👤 تسجيل الدخول وتسجيل الحساب (Graduates – Companies – Admins).  
- 📋 إدارة البروفايلات (Students Profiles & Company Profiles).  
- 💼 الشركات تقدر تنشر وظائف، والخريجين يقدموا عليها.  
- 📨 نظام شكاوي (Complaints System) مع status update (pending → approved → rejected).  
- 🔔 Notifications مرتبطة بالشكاوي والوظائف.  
- 🌍 دعم الترجمة (Arabic / English).  

---

## 📂 Database Design
- **Users Table** → تخزين البيانات الأساسية (name, email, role).  
- **Profiles Table** → مرتبطة بـ user_id لتوسيع البيانات.  
- **Companies Table** → بيانات الشركات.  
- **Jobs Table** → وظائف مرتبطة بالشركات.  
- **Applications Table** → many-to-many بين users و jobs.  
- **Complaints Table** → مرتبطة بـ user_id + status.  
- **Notifications Table** → مرتبطة بالمستخدم أو الوظيفة.  

---

## 🚀 Installation & Run

### Backend (Laravel)
```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
