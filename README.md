## 🎨 Paint Order System — Streamlit Web Application

This project is a fully‑featured **paint ordering system** built with **Python**, **Streamlit**, and **SQLite**, designed for artists working on mural projects.  
It provides a clean, intuitive interface for placing, viewing, updating, deleting, and duplicating paint orders, with live metadata and sustainability information.

---

## 🚀 Features

### ✔ **Artist Login System**
Artists log in with:
- First name  
- Last name  
- Studio number  

Session state keeps each artist’s session isolated.

### ✔ **Place Orders**
- Select paint base, size, additives, and additive parts  
- Live description + sustainability metadata  
- Quantity selector  
- Price breakdown  
- Preview + confirmation workflow  

### ✔ **View Orders**
- Search by artist  
- Filter by paint base  
- DataFrame display  
- Summary metrics  
- Quick actions: Edit, Delete, Duplicate  

### ✔ **Update Orders**
- Search + filter  
- DataFrame of matching orders  
- Radio‑list selector  
- Side‑by‑side comparison (old vs new)  
- Full edit form with metadata  
- Confirmation workflow  

### ✔ **Delete Orders**
- Search + filter  
- DataFrame view  
- Radio‑list selector  
- Full order summary before deletion  
- Confirmation workflow  

### ✔ **Duplicate Orders**
One‑click duplication from the View Orders screen.

### ✔ **SQLite Database Persistence**
All orders and menu metadata are stored in:
```
orders_v2.db
```

### ✔ **TXT Logging (Assignment Requirement)**
Every CREATE, UPDATE, and DELETE action is logged to:
```
orders_log.txt
```
This provides a human‑readable audit trail.

### ✔ **Logout System**
Artists can log out and switch accounts instantly.

---

## 📁 Project Structure

```
sprint-project-gui-final-system/
│
├── streamlit_app_v7.py        # Main Streamlit application
├── Artist.py                  # Artist class
├── Paint.py                   # Paint class
├── PaintMenu.py               # Paint menu + metadata loader
│
├── orders_v2.db               # SQLite database (auto-created)
├── orders_log.txt             # TXT log file (auto-created)
│
└── README.md                  # Project documentation

```

---

## 🗄️ Data Persistence

### **Primary Storage — SQLite**
All orders are stored in `orders_v2.db` with fields:
- Artist info  
- Timestamp  
- Paint base  
- Size  
- Additives  
- Additive parts  
- Cost  
- Quantity  

### **Secondary Storage — TXT Logging**
To satisfy assignment requirements, every CRUD action is logged in:
```
orders_log.txt
```

Each entry includes:
- Action (CREATE / UPDATE / DELETE)  
- Order ID  
- Artist  
- Studio  
- Timestamp  
- Paint details  
- Cost + quantity  

---

## 🌱 Sustainability Metadata

Each paint base and additive includes:
- Description  
- Sustainability information  
- Origin (optional)

Metadata is loaded from the `menu_items` table in SQLite and displayed live under dropdowns.

---

## 🌐 Deployment

This app is deployed on **Streamlit Cloud**.

Deployment steps:
1. Push code to GitHub  
2. Connect repo to Streamlit Cloud  
3. Set main file to `streamlit_app_v7.py`  
4. No `requirements.txt` needed unless you add external packages  

---

## 📦 Requirements

Streamlit Cloud includes Streamlit by default.  
If you want a `requirements.txt`, use:

```
streamlit
```

Add more only if you install additional packages.

---

## 🧩 Technologies Used

- **Python 3**
- **Streamlit**
- **SQLite3**
- **Session State**
- **OOP Architecture**

---

## 📘 Potential Future Enhancements

- Add CSV export
- Add a TXT log viewer page
- Add admin dashboard
- Add color‑coded sustainability badges

---

## ✒️ Author

Developed by **Jeet Modi**  
Built with a focus on clean UI, robust data handling, and intuitive artist workflows.

---

If you'd like, I can also generate:

- **A polished `.gitignore`**  
- **A `requirements.txt` optimized for Streamlit Cloud**  
- **A version of the README with screenshots**  
- **A version formatted for Canvas / PDF submission**

Just tell me what you want next.
