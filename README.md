# **kindergarten Managment System**

A brief description of your project here.

---

## **Requirements**
Before starting, ensure your system meets the following requirements:
- PHP >= 8.0
- Composer
- Node.js (with npm)
- MySQL (or your database of choice)

---

## **Installation Guide**

Follow these steps to set up the project on your local machine:

### **Step 1: Clone the Repository**

git clone <repository-url>
cd <project-folder>


---

### **Step 2: Install Composer**

#### **What is Composer?**
Composer is a dependency manager for PHP that handles libraries and packages.

#### **Install Composer**
1. Visit [getcomposer.org/download](https://getcomposer.org/download) for installation instructions.
2. Alternatively, use the command line:
   - On Linux/MacOS:
     
     curl -sS https://getcomposer.org/installer | php
     sudo mv composer.phar /usr/local/bin/composer
     
   - On Windows:
     - Download and run the Composer installer from [here](https://getcomposer.org/Composer-Setup.exe).

3. Verify installation:
   
   composer --version
   

---

### **Step 3: Install PHP Dependencies**
Run the following command to install Laravel dependencies:

composer install


---

### **Step 4: Set Environment Variables**
1. Copy the `.env.example` file to create your `.env` file:
   
   cp .env.example .env
   
2. Edit the `.env` file to configure your database and other settings:
   dotenv
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_user
   DB_PASSWORD=your_database_password
   

---

### **Step 5: Generate Application Key**
Run this command to generate the application key:

php artisan key:generate


---

### **Step 6: Install Node.js and npm**
#### **What is Node.js?**
Node.js is a JavaScript runtime that allows you to run npm, which is used to manage frontend dependencies.

#### **Install Node.js**
1. Visit [nodejs.org](https://nodejs.org/) and download the LTS version.
2. Verify installation:
   
   node -v
   npm -v
   

---

### **Step 7: Install Frontend Dependencies**
Run the following command to install all required frontend dependencies:

npm install


---

### **Step 8: Compile Assets**
To compile assets (CSS, JS, etc.), run:
- For development:
  
  npm run dev
  
- For production (optimized build):
  
  npm run prod
  

---

### **Step 9: Run Migrations**
Run the database migrations to set up your database structure:

php artisan migrate


---

### **Step 10: Start the Development Server**
Run the following command to start the Laravel development server:

php artisan serve


Open your browser and navigate to:

http://127.0.0.1:8000


---

## **Additional Commands**

### **Clear Caches**
To clear application caches:

php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear


---

## **Common Issues and Troubleshooting**

### **1. CSS or JS Not Working**
If the CSS or JavaScript is not loading properly:
- Ensure you’ve run `npm install` and `npm run dev`.
- Verify that the `public/css` and `public/js` directories contain the compiled assets.

### **2. Permission Issues**
If you encounter file permission issues, run:

chmod -R 775 storage bootstrap/cache


---
