# LMS-UTC

A Learning Management System built for the Universal Training College (UTC) using Laravel 8. The platform supports course enrollment, virtual classrooms, Zoom-integrated live sessions, and a structured assessment workflow for students and teachers.

## Features

- **Course Catalog** -- Browse courses organized by categories and units with downloadable materials
- **Virtual Classrooms** -- Dedicated classroom spaces with posts, announcements, and file sharing
- **Zoom Integration** -- Schedule and join live meetings directly from the platform
- **Student Enrollment** -- Multi-step enrollment workflow with activation and progress tracking
- **Assessment System** -- Course unit assessments with progress tracking per student
- **Calendar** -- Integrated event calendar for scheduling classes and deadlines
- **User Roles** -- Admin dashboard, teacher portal, and student interface with role-based access
- **File Management** -- Upload and manage course materials, post attachments, and user documents
- **Admin Panel** -- Manage users, courses, classrooms, announcements, and site settings

## Tech Stack

- **Backend:** PHP 7.3+ / 8.0, Laravel 8
- **Frontend:** Blade templates, Tailwind CSS, Laravel Mix
- **Database:** MySQL
- **Authentication:** Laravel Breeze
- **Live Sessions:** Zoom API
- **Image Processing:** Intervention Image
- **Rich Text:** PHP Quill Renderer
- **JWT:** Firebase PHP-JWT

## Prerequisites

- PHP >= 7.3
- Composer
- MySQL 5.7+
- Node.js & npm

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/mhmalvi/lms-utc.git
   cd lms-utc
   ```

2. **Install dependencies**
   ```bash
   composer install
   npm install
   ```

3. **Configure environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Update `.env`** with your database credentials and Zoom API keys.

5. **Import the database** (if using the provided SQL dump)
   ```bash
   mysql -u root -p your_database < ntanswed_demo.sql
   ```

6. **Run migrations** (alternative to SQL import)
   ```bash
   php artisan migrate --seed
   ```

7. **Build frontend assets**
   ```bash
   npm run dev
   ```

8. **Start the development server**
   ```bash
   php artisan serve
   ```

The application will be available at `http://localhost:8000`.

## Project Structure

```
app/
  Http/Controllers/
    Admin/       # Admin panel controllers
    Auth/        # Authentication controllers
  Models/        # Eloquent models (Course, Classroom, Enrollment, etc.)
routes/
  admin.php      # Admin routes
  api.php        # API routes
  web.php        # Public web routes
resources/       # Blade views and frontend assets
database/        # Migrations, seeders, and SQL dumps
```

## License

MIT
