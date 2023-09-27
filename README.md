<!DOCTYPE html>
<html>
<head>
  
</head>
<body style="background-color: #f3f3f3; padding: 20px; font-family: Arial, sans-serif;">

<h1 style="color: #333;">User-Registration-FastAPI</h1>

<p>This is a simple FastAPI-based web application that allows users to register with their basic information and upload a profile picture. Registered user data is stored in a User table in PostgreSQL database, and profile pictures are stored in another table Profile in same PostgreSQL database.</p>
<h2 style="color: #555;">Requirements</h2>

<p>Before running this application, ensure you have the following dependencies installed:</p>

<ol>
  <li>Python 3.7+</li>
  <li>PostgreSQL (with required database and table set up)</li>
</ol>
<h2 style="color: #555;">Installation</h2>

<ol>
  <li>Clone this repository to your local machine.</li>
  <pre><code>git clone https://github.com/your-username/your-repo.git</code></pre>

  <li>Navigate to the project directory.</li>
  <pre><code>cd your-repo</code></pre>

  <li>Install the required Python packages using pip.</li>
  <pre><code>pip install -r requirements.txt</code></pre>
</ol>

<h2 style="color: #555;">Environment Variables</h2>

<p>Before running the application, you need to set up the environment variables.</p>

<ol>
  <li>Create an environment file named .env in the project root directory.</li>
  <li>Provide the required values for each environment variable in the .env.sample file.</li>
</ol>

<h2 style="color: #555;">Usage</h2>

<p>To start the FastAPI application, run the following command:</p>

<pre><code>uvicorn main:app --host 0.0.0.0 --port 8000 --reload</code></pre>

<p>Make sure to replace <code>main</code> with the name of your main Python file if it differs.</p>

<h2 style="color: #555;">Endpoints</h2>

<ol>
  <li>
    <h3>User Registration</h3>
    <p><strong>URL:</strong> /register/ (POST)</p>
    <p><strong>Description:</strong> Register a new user with their information and upload a profile picture.</p>
    <h4>Request Body:</h4>
    <pre><code>json
{
  "first_name": "John",
  "password": "your_password",
  "email": "john@example.com",
  "phone": "123-456-7890",
  "profile_picture": [file_upload]
}</code></pre>
    <h4>Response:</h4>
    <pre><code>json
{
  "user_id": 1,
  "message": "User registered successfully"
}</code></pre>
  </li>

  <li>
    <h3>Get User Details</h3>
    <p><strong>URL:</strong> /user/{user_id}/ (GET)</p>
    <p><strong>Description:</strong> Retrieve user details, including their profile picture.</p>
    <h4>Response:</h4>
    <pre><code>json
{
  "user_id": 1,
  "first_name": "John",
  "email": "john@example.com",
  "phone": "123-456-7890",
  "profile_picture": "path_to_profile_picture"
}</code></pre>
  </li>
</ol>


</body>
</html>
