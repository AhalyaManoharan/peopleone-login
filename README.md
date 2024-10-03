# peopleone-login
<h3>Basic User Authentication System (PHP & MySQL)</h3>

<h4>Objective:</h4>
<p>This project implements a basic user authentication system using Core PHP (Vanilla PHP) and MySQL. 
It provides functionalities for user registration, login, and logout with a focus on security features such as password hashing and protection against CSRF and SQL Injection.</p>

<h4>Steps to Set Up the Project:</h4>

<h4>Step 1: Clone the Repository</h4>
<p>Run the following commands to clone and navigate to the project:</p>
<p><code>git clone https://github.com/AhalyaManoharan/peopleone-login</code><br>
<code>cd peopleone-login</code></p>

<h4>Features:</h4>
<p><strong>User Registration:</strong> Users can register using their username, email, and password.</p>
<p><strong>User Login:</strong> Users can log in using their username or email and password.</p>
<p><strong>User Logout:</strong> Users can log out, and their session will be destroyed.</p>
<p><strong>Remember Me:</strong> An optional "Remember Me" feature enables persistent login sessions using cookies.</p>
<p><strong>Security Features:</strong> Passwords are hashed using PHP's <code>password_hash()</code> function, inputs are sanitized to prevent SQL Injection, and Cross-Site Request Forgery (CSRF) protection is in place.</p>

<h4>1. Registration</h4>
<p><strong>File:</strong> <code>register.php</code></p>
<p>The registration page allows users to sign up with a username, email, and password. Input data is validated as follows:</p>
<p>Username must be unique.<br>
Email must be in a valid format.<br>
Password must meet strength criteria (minimum 6 characters).</p>
<p>Passwords are stored securely using PHP's <code>password_hash()</code> function.</p>

<h4>2. Login</h4>
<p><strong>File:</strong> <code>login.php</code></p>
<p>The login page allows users to authenticate using either username or email along with their password. Sessions are used to manage user authentication after a successful login.</p>
<p>If the "Remember Me" checkbox is selected, a persistent cookie (<code>remember_me</code>) is set to store the user’s session even after the browser is closed.</p>

<h4>3. Logout</h4>
<p><strong>File:</strong> <code>logout.php</code></p>
<p>When users log out, the session is destroyed using <code>session_destroy()</code>. If a "Remember Me" cookie is set, it is also cleared, ensuring that persistent login is disabled.</p>

<h4>4. Security Considerations</h4>
<p><strong>Password Hashing:</strong> Passwords are securely hashed using PHP's <code>password_hash()</code> function to prevent storing plain-text passwords in the database.</p>
<p>Password verification during login is handled with <code>password_verify()</code>.</p>

<h4>How to Test "Remember Me":</h4>
<p>Log in with valid credentials.<br>
Check the "Remember Me" checkbox.<br>
Close the browser and reopen the login page. You should still be logged in.</p>

<h4>Conclusion:</h4>
<p>This basic user authentication system demonstrates secure login, registration, and logout functionality using PHP and MySQL, with added security layers like CSRF protection, SQL injection prevention, and password hashing. The "Remember Me" feature provides persistent login functionality using cookies.</p>
