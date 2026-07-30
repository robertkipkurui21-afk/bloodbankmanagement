# Blood Bank Management System

![developer](https://img.shields.io/badge/Maintained%20By%20%3A-KahlubDev-blue)
![original developer](https://img.shields.io/badge/Original%20Author%20%3A-Sumit%20Kumar-red)

---

## Credits & Acknowledgments
This project is a modernized version of the original **Blood Bank Management System** created by **Sumit Kumar**. 

* **Original Repository:** [sumitkumar1503/bloodbankmanagement](https://github.com/sumitkumar1503/bloodbankmanagement)
* **Modifications in this version:** Updated setup compatibility for Python 3.12+, removed hardcoded secrets in favor of `django-environ`, fixed legacy dependency issues, and updated setup instructions.

---

## Screenshots

### Homepage
![homepage snap](https://github.com/sumitkumar1503/bloodbankmanagement/blob/master/static/screenshot/homepage.png?raw=true)

### Admin Dashboard
![dashboard snap](https://github.com/sumitkumar1503/bloodbankmanagement/blob/master/static/screenshot/admindashboard.png?raw=true)

### Blood Donation 
![invoice snap](https://github.com/sumitkumar1503/bloodbankmanagement/blob/master/static/screenshot/blooddonation.png?raw=true)

### Blood Request
![doctor snap](https://github.com/sumitkumar1503/bloodbankmanagement/blob/master/static/screenshot/bloodrequest.png?raw=true)

### Logout
![logout snap](https://github.com/sumitkumar1503/bloodbankmanagement/blob/master/static/screenshot/logout.png?raw=true)

---

## Features

### Admin
* Create an Admin account using:
  ```powershell
  py manage.py createsuperuser
  ```
* View overall blood stock units by group, total donors, total patients, and pending/approved requests from the dashboard.
* View, update, or delete Donors and Patients.
* Approve or reject blood donation requests (approving adds units to the stock).
* Approve or reject blood requests (approving deducts units from stock).
* View request history and manually update stock units for specific blood groups.

### Donor
* Register an account and log in.
* Submit blood donation requests and track approval status (Pending, Approved, Rejected).
* Request blood from stock when needed.
* View dashboard metrics for requests made, approved, pending, and rejected.

> **NOTE:** Donors can both donate blood and request blood.

### Patient
* Register an account (no admin approval required for signup).
* Request blood of a specific group and unit count.
* Track request history and status via the patient dashboard.

---

## Setup & Running the Project

### Prerequisites
* Python 3.12+ installed (ensure **Add Python to PATH** is checked during installation).
* Git installed.

### Installation Steps

1. **Clone the Repository:**
   ```powershell
   git clone https://github.com/KahlubDev/bloodbankmanagement.git
   cd bloodbankmanagement
   ```

2. **Install Dependencies:**
   ```powershell
   py -m pip install -r requirements.txt
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the project root directory alongside `manage.py` with the following variables:
   ```env
   SECRET_KEY=your-secret-key-here
   DEBUG=True
   ALLOWED_HOSTS=127.0.0.1,localhost
   EMAIL_HOST_USER=your_email@gmail.com
   EMAIL_HOST_PASSWORD=your_app_password
   EMAIL_RECEIVING_USER=receiver_email@gmail.com
   ```

4. **Apply Database Migrations:**
   ```powershell
   py manage.py migrate
   ```

5. **Start the Development Server:**
   ```powershell
   py manage.py runserver
   ```

6. **Access the App:**
   Open your browser and navigate to:
   ```text
   http://127.0.0.1:8000/
   ```
