<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/9/94/Jata_MalaysiaV2.svg" 
       alt="MyPelantikan Logo" 
       width="60"; vertical-align:middle;" />
</p>

# <p align="center">MyPelantikan</p>

A full-stack profile management system built with Vue 3 and Laravel.

## ✨ Overview

MyPelantikan helps manage user profiles and service history in a structured and efficient way. 
Built with a clean UI and scalable backend, it focuses on performance, usability, and maintainability.

## 🧱 Tech Stack

**Backend**
- Laravel
- Eloquent ORM
- REST API
- API Resources

## 📁 Project Structure
```bash
MyPelantikan/
├── front-end/
│ ├── assets/
│ ├── components/
│ ├── views/
│ ├── router/
│ ├── store/
│ └── layouts/
│
├── back-end/
│ ├── app/
│ │ ├── Models/
│ │ ├── Http/
│ │ │ ├── Controllers/
│ │ │ └── Resources/
│ ├── routes/api.php
│ ├── database/
│ └── config/
│
└── README.md
```
## ⚙️ Features

- Dynamic form builder  
- Editable data tables (filter, sort, group)  
- Profile & service history management  
- REST API integration  
- Server-side pagination  
- Reusable UI components  
- PDF export  

## 🔌 Installation

### Prerequisites

Ensure you have the following installed:
- PHP (Recommended version: ^8.4 or higher)
- Composer
- Node.js & NPM (Recommended version: 16.x or higher)
- MySQL or MariaDB

### 1. Clone repository
```bash
git clone --recursive https://github.com/lqmnwido/mypelantikan.git
cd mypelantikan
```
***If you have already cloned the repository without the `--recursive` flag, run the following command to initialize and update the submodules:*** 
``` bash
git submodule update --init --recursive
```

### 2. Backend (Laravel)
```bash
cd back-end
composer install
cp .env.example .env
```

**Generate Application Key**
``` bash
    php artisan key:generate
```

**Database Configuration**
- Create a new database in your local environment (e.g., named `mypelantikan`).
- Open the `.env` file and update the database settings:
``` bash 
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=mypelantikan
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
```

**Run Migrations and Seeders**
``` bash
    php artisan migrate --seed
    php artisan serve
```
**Link Storage**
    Create a symbolic link from `public/storage` to `storage/app/public`:
```bash
    php artisan storage:link
```

This command uses `concurrently` to run the following services in parallel:
- **Scheduler:** `to run scheduled tasks`
``` bash
    php artisan schedule:work 
```

### 3. Frontend (Vue)
``` bash
cd front-end
npm install
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory. You can copy the contents from `.env.production` as a starting point:
```bash
cp .env.production .env
```
Open the `.env` file and adjust the following variables:

#### Authentication Modes
The project supports different authentication modes via `VUE_APP_DEFAULT_AUTH`:
- **Fake Backend (Default)**: Set `VUE_APP_DEFAULT_AUTH=fakebackend`. This allows you to log in without a real API using:
  - **Email**: `admin@themesbrand.com`
  - **Password**: `123456`
- **Real Backend**: Set `VUE_APP_DEFAULT_AUTH=authservice` (or as configured in your services) and provide the `VUE_APP_APIKEY`.

#### API Configuration
- `VUE_APP_APIKEY`: The base URL of your API (e.g., `http://{{api-url}}/api/v1/`)
- `VUE_GAMBAR_URL`: The storage URL for images (e.g., `http://{{api-url}}/storage`)

### 4. Run the Development Server
Start the local development server with:
```bash
npm run serve
```

## 🔗 API
- RESTful API via Laravel
- Axios for frontend requests
- JSON responses using API Resources

## 🧠 Concepts

### Vue
- props – pass data
- data() – state
- methods – actions
- computed – derived values
- watch – react to changes

### Laravel
- MVC structure
- Eloquent relationships
- Controllers for logic
- Resources for API formatting

## 🚀 Roadmap
Role-based authentication
Dashboard & analytics
File management
Notifications

## 👨‍💻 Author
Luqman Hafiz
Full Stack Developer (Vue + Laravel)

## ⭐ Support
If you find this useful, give it a ⭐ on GitHub 👍

