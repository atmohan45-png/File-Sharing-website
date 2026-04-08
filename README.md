📁 SyncRoom — Real-Time File Sharing Web App

SyncRoom is a lightweight Flask-based file sharing web application that allows users to create temporary rooms and instantly share files with others in real time.

It supports multi-user rooms, file expiry, and live activity tracking.

🚀 Features
🏠 Create unique file-sharing rooms (6-digit code)
📤 Upload multiple files at once
⏳ Auto-delete files after a custom expiry time
🔗 Share room code with others instantly
👥 Live user count (real-time presence tracking)
🗑️ Delete files manually
🔐 User authentication (Register/Login system)
📥 Download shared files بسهولة
🧹 Background cleanup of expired files
🛠️ Tech Stack

Backend:

Python (Flask)
Flask-SQLAlchemy
Flask-Login

Database:

SQLite (saladroom.db)

Frontend:

HTML (Jinja templates)
CSS
JavaScript (for API calls & live updates)
📂 Project Structure
SyncRoom/
│── app.py              # Main Flask application
│── models.py          # Database models
│── uploads/           # Stored files (auto-created)
│── templates/         # HTML pages
│── static/            # CSS & JS
│── saladroom.db       # SQLite database
│── README.md
⚙️ Installation & Setup
1. Clone the repository
git clone https://github.com/your-username/syncroom.git
cd syncroom
2. Install dependencies
pip install flask flask_sqlalchemy flask_login werkzeug
3. Run the application
python app.py
4. Open in browser
http://localhost:5000
🔑 How It Works
🏠 Room Creation
User creates a room
A unique 6-character code is generated
📤 File Upload
Files are uploaded to:
/uploads/<room_code>/
⏳ Expiry System
Each file has expiry time (default: 5 mins)
-1 → permanent file
Background thread deletes expired files automatically
👥 Live Users
Uses session-based tracking
Heartbeat API updates active users every few seconds
🔌 API Endpoints
Endpoint	Method	Description
/create-room	POST	Create new room
/room/<code>	GET	Join room
/api/check_room/<code>	GET	Check if room exists
/api/room/<code>/upload	POST	Upload files
/api/room/<code>/files	GET	Get file list
/api/room/<code>/delete/<filename>	POST	Delete file
/api/room/<code>/heartbeat	POST	Update active users
/download/<code>/<filename>	GET	Download file
🔐 Authentication System
Users can:
Register
Login
Logout
Passwords are securely hashed using Werkzeug
🧠 Background Tasks

A separate thread handles:

🗑️ Deleting expired files
🧹 Removing inactive users (after 30 seconds)
⚠️ Important Notes
No file size limit currently (can be added)
Files are stored locally (not cloud-based)
Not production-ready security (needs improvements)
📌 Future Improvements
☁️ Cloud storage (AWS S3 / Firebase)
🔐 Room password protection
📊 Upload progress bar
📁 Drag & drop UI
📦 File compression before upload
🌐 Deployment (Render / Railway / VPS)
🔒 HTTPS & production security
🤝 Contributing
Fork the project
Create your feature branch
Commit your changes
Push to GitHub
Open a Pull Request
📄 License

This project is licensed under the MIT License.
