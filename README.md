Blog API and Frontend Application
This project is a simple, full-stack blog application featuring a PHP backend with a MySQL database and a pure HTML/JavaScript frontend. It demonstrates basic CRUD (Create, Read, Update, Delete) functionality with a RESTful API and a responsive user interface.

🚀 Features
Create Posts: Add new blog posts with a title and content.

Read Posts: View all existing blog posts on the main page.

Update Posts: Edit the title and content of an existing post.

Delete Posts: Remove posts from the database.

View Full Post: Click a post's title to view its full content in a modal.

Search Posts: A search bar allows you to filter posts by title or content in real-time.

Responsive Design: The frontend is built with Tailwind CSS to ensure a great user experience on all devices.

Modal Dialogs: Custom modal dialogs for editing, viewing, confirming deletion, and displaying messages.

🛠️ Technology Stack
Backend: PHP, MySQL

Frontend: HTML5, JavaScript, Tailwind CSS

📝 Setup Instructions
Follow these steps to get the application running on your local machine.

1. Backend Setup
Database:

Create a new MySQL database (e.g., blog_db).

Create a posts table with the following structure:

CREATE TABLE `posts` (
  `id` int(11) PRIMARY KEY AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `content` text NOT NULL,
  `created_at` timestamp NOT NULL DEFAULT current_timestamp()
);

Configuration:

Open config/Database.php.

Update the database connection details:

private $host = "localhost";
private $db_name = "your_database_name"; // e.g., blog_db
private $username = "your_username";
private $password = "your_password";

API Token:

The backend requires an Authorization token for POST, PUT, and DELETE requests.

The hardcoded token is 123456789SECRET. You can change this in api/posts.php to a more secure value if needed.

2. Frontend Setup
File Placement:

Place the index.html file in a directory that is served by your local web server (e.g., inside an htdocs or www folder).

API URL:

Open index.html and locate the JavaScript section.

Ensure the apiUrl variable is pointing to your backend:

const apiUrl = 'http://localhost/blog_api/api/posts.php';

(Adjust the path if your project structure is different).

API Token:

Ensure the API_TOKEN in index.html matches the token in your api/posts.php file.

const API_TOKEN = '123456789SECRET';

🚀 Usage
Start your local server: Ensure your Apache or Nginx server is running.

Open the frontend: Navigate to http://localhost/your-project-folder/index.html in your web browser.

Interact:

Use the "Create a New Post" form to add new posts.

Posts will appear below the form.

Click a post's title to view its full content.

Use the "Edit" and "Delete" buttons to modify or remove posts.

Use the search bar to filter posts.
