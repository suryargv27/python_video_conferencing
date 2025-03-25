# Video Conferencing App

## Overview
This is a Python-based video conferencing application that supports:
- Real-time video communication
- Text chat functionality
- File transfer between clients

The application uses **socket programming** for network communication and **OpenCV** for handling video streaming. It supports multiple clients and allows private/unicast as well as broadcast communication for both chat and file transfer.

## Features
- **Real-time video conferencing**
- **Chat functionality** with private messaging
- **File transfer system**
- **GUI-based client interface** using Tkinter
- **Multi-client support**

## Tech Stack
- **Python**
- **Socket Programming**
- **OpenCV**
- **Tkinter (GUI)**
- **Pickle & Struct (for data serialization)**

## Installation & Setup

### Prerequisites
Ensure you have the following installed:
- Python 3.x
- OpenCV (`cv2`)
- Tkinter

### Steps to Install & Run
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your_username/video-conferencing-app.git
   cd video-conferencing-app
   ```
2. **Install required dependencies**:
   ```bash
   pip install opencv-python numpy
   ```
3. **Start the server**:
   ```bash
   python server.py
   ```
4. **Start the client** (Run for each client instance):
   ```bash
   python client.py
   ```

## How It Works
### Server (`server.py`)
- Listens for connections on three different ports:
  - **Port 7777**: Video streaming
  - **Port 7778**: Chat
  - **Port 7779**: File transfer
- Handles multiple clients simultaneously using threading
- Manages private and broadcast communication for chat and file transfer

### Client (`client.py`)
- Connects to the server
- Captures video from the webcam and transmits it to the server
- Receives video frames from other clients and displays them using OpenCV
- Provides GUI for chat and file transfer

## File Structure
```
├── client.py         # Main client application
├── server.py         # Server to manage video, chat, and file transfer
├── network.py        # Handles data transmission (video, chat, files)
├── interface.py      # GUI implementation for the client
├── black.jpg         # Placeholder image for video
└── README.md         # Documentation
```

## Usage
### Video Conferencing
1. Clients join the video room automatically when they start `client.py`
2. Video is captured and transmitted in real time
3. Use **Next/Prev buttons** in GUI to switch between clients

### Chat
- **Broadcast**: Send messages to all connected clients
- **Unicast**: Send private messages by selecting a client from the dropdown

### File Transfer
- **Broadcast**: Send a file to all connected clients
- **Unicast**: Send a file to a specific client

## Contributing
Feel free to contribute by submitting pull requests. Ensure your code follows best practices and is well-documented.

## License
This project is licensed under the MIT License.

## Author
[Your Name](https://github.com/your_username)

---
This README provides detailed setup instructions, explanations of each component, and usage guidelines. Let me know if you need any modifications!

