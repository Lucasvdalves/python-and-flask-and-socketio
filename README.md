# Python, Flask & Socket.IO

This repository is a demonstration of integrating Python, Flask, and Socket.IO to build a real-time web application. Everything you need is provided in this one file, including all code samples and setup instructions.

---

## Project Overview

- **Real-Time Communication:** Uses Socket.IO for live, bidirectional communication.
- **Flask Backend:** Built on the lightweight and flexible Flask web framework.
- **All-in-One Setup:** All necessary code and instructions are included below for a quick and easy setup.

---

## File Contents

Below are the complete contents for each file you need to create.

### 1. `app.py`

Create a file named `app.py` with the following content:

```python
from flask import Flask, render_template
from flask_socketio import SocketIO, send

app = Flask(__name__)
app.config['SECRET_KEY'] = 'secret!'
socketio = SocketIO(app)

@app.route('/')
def index():
    return render_template('index.html')

@socketio.on('message')
def handle_message(msg):
    print('Message: ' + msg)
    send(msg, broadcast=True)

if __name__ == '__main__':
    socketio.run(app, debug=True)
