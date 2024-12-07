### Elixir: A Blood Donation Platform

**Description:**
Elixir is a web-based platform designed to connect blood donors and donees in real-time. It automates the search for available donors, enabling donees to focus on patient care rather than the logistics of finding a donor.

The app includes:
1. **Login System:** Separate logins for donors and donees.
2. **Donor Search:** Donees can request blood by specifying blood type, location, and distance. The app searches for available donors automatically.
3. **Chat System:** Once a donor accepts, a real-time chat is initiated between the donor and the donee.
4. **Admin Tools:** Easy extensibility for adding admin features like monitoring donor and donee activities.

---

### **Folder Structure**
- **`frontend/`**: Contains React-based code for the user interface.
  - **`src/`**:
    - **`assets/`**: Images and logos.
    - **`components/`**: Reusable components like `Navbar`, `Chat`, and `DonorDashboard`.
    - **`pages/`**: Specific pages like `Login`, `BloodRequest`, `Home`.
    - **`Socket.js`**: Handles WebSocket connections.
  - **`App.js`**: Main entry point for the frontend application.
- **`backend/`**: Contains Flask-based API logic for the server.
  - **`routes/`**: Contains route definitions for donors, donees, and admin actions.
  - **`app.py`**: Main server file for starting the Flask backend.
  - **`database/`**: Database models and configurations.

---

### **Necessary Installations**
#### **Frontend:**
1. Install **Node.js** (includes npm).
   - [Download and install Node.js](https://nodejs.org/).
2. Required npm packages:
   - **react-router-dom**: For routing.
   - **axios**: For API requests.
   - **socket.io-client**: For WebSocket communication.
   - **react-icons**: For using icons in the UI.
   ```bash
   npm install react-router-dom axios socket.io-client react-icons
   ```
3. To install all dependencies at once:
   ```bash
   npm install
   ```

#### **Backend:**
1. Install **Python 3.x**.
2. Required Python packages:
   - **Flask**: Backend framework.
   - **Flask-SocketIO**: For WebSocket communication.
   - **Flask-Cors**: For enabling cross-origin requests.
   - **Flask-JWT-Extended**: For authentication.
   - **SQLAlchemy**: For database interactions.
   - **eventlet**: For asynchronous Socket.IO.
   - **dotenv**: For managing environment variables.
   ```bash
   pip install flask flask-socketio flask-cors flask-jwt-extended sqlalchemy eventlet python-dotenv
   ```
3. To install all dependencies at once:
   ```bash
   pip install -r requirements.txt
   ```

---

### **How the Code Works**
1. **Frontend Workflow**:
   - Users access the login page.
   - Depending on the user type (donor or donee), they are redirected to respective dashboards after logging in.
   - Donees can raise blood requests and view donor responses.
   - A real-time chat system allows communication between donors and donees.

2. **Backend Workflow**:
   - Donee requests are processed through a `POST /donees/request` route.
   - Available donors are notified in real-time using Socket.IO.
   - Chat functionality is implemented using WebSockets to manage rooms dynamically.

---

### **Steps for Running the Project Locally**
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd Elixir
   ```
2. **Backend Setup**:
   - Navigate to the backend directory:
     ```bash
     cd backend
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - Start the Flask server:
     ```bash
     python app.py
     ```
3. **Frontend Setup**:
   - Navigate to the frontend directory:
     ```bash
     cd ../frontend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the React server:
     ```bash
     npm start
     ```
---

### **Aim of the Project**
This project aims to solve the critical problem of blood donation and availability by leveraging technology to create an intuitive and efficient platform for connecting donors and donees.
