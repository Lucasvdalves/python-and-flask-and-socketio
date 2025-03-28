# 🔌 Python, Flask & Socket.IO

## 📌 About the Project
This project demonstrates real-time communication between a Flask server and web clients using Socket.IO. It serves as a base for chat apps, real-time dashboards, or notification systems.

## 💡 Features
- Real-time bidirectional communication via WebSockets
- Flask-based backend
- Simple and clean frontend interface
- Broadcast messages to all connected users

## 🛠️ Technologies Used
- Python 3
- Flask
- Flask-SocketIO
- HTML5 & JavaScript

## 📁 Folder Structure
```
├── app.py
├── requirements.txt
├── /templates
│   └── index.html
```

## 🚀 Getting Started

1. **Clone the Repository**
```bash
git clone https://github.com/Lucasvdalves/python-and-flask-and-socketio.git
cd python-and-flask-and-socketio
```

2. **Install Dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the Application**
```bash
python app.py
```

4. **Access in Browser**
Go to: [http://localhost:5000](http://localhost:5000)

## 🔄 How It Works
- Users connect to the server via Socket.IO.
- Messages sent by one user are broadcast to all connected clients.
- All logic is handled on the `app.py` backend and `index.html` frontend.

## 🎯 Future Improvements
- User nickname support
- Chat room separation
- Message persistence (e.g., SQLite,
