
# Django and React Project Setup

## Prerequisites
Before starting, make sure you have the following installed on your machine:
- Python (>=3.8)
- Node.js (>=14.x) and npm (Node Package Manager)
- pip (Python Package Installer)
- Virtualenv (optional but recommended)

## Project Structure
```
project_root/
  backend/   # Django backend folder
    .env     # Environment variables for backend (e.g., HUBSPOT_API_KEY)
  frontend/  # React frontend folder
```

---

## Setting Up the Backend (Django)

1. **Navigate to the backend folder:**
   ```bash
   cd backend
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` file:**
   In the `backend` folder, create a file named `.env` and add your environment variables:
   ```env
   HUBSPOT_API_KEY=your_hubspot_api_key_here
   ```

5. **Run database migrations:**
   ```bash
   python manage.py migrate
   ```

6. **Start the Django development server:**
   ```bash
   python manage.py runserver
   ```

---

## Setting Up the Frontend (React)

1. **Navigate to the frontend folder:**
   ```bash
   cd ../frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the React development server:**
   ```bash
   npm start
   ```

This will start the React application on `http://localhost:3000` by default.

---

## Running the Full Project

1. **Start the backend server:**
   Navigate to the `backend` folder and run:
   ```bash
   python manage.py runserver
   ```

2. **Start the frontend server:**
   Open a new terminal, navigate to the `frontend` folder, and run:
   ```bash
   npm start
   ```

---

## Notes
- The `.env` file in the `backend` folder should **never be committed to version control**. Make sure to add it to `.gitignore`.
- Ensure that `HUBSPOT_API_KEY` is replaced with the actual API key you receive from HubSpot.

---

## Troubleshooting

### Backend
- If you encounter issues with dependencies, ensure your virtual environment is activated and try reinstalling packages using:
  ```bash
  pip install -r requirements.txt
  ```

### Frontend
- If `npm start` fails, try deleting the `node_modules` folder and reinstalling:
  ```bash
  rm -rf node_modules
  npm install
  ```
