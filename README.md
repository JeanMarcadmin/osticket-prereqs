<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket - Prerequisites and Installation Guide</h1>

This guide provides step-by-step instructions to install and configure osTicket, a powerful open-source support ticket system, using Microsoft Azure and Windows 10.

---

## 🎥 Video Demonstration

- [YouTube: How To Install osTicket with Prerequisites]([https://www.youtube.com](https://www.youtube.com/watch?v=K7T_JjvEamg&t=1s) *

---

## 🧰 Environments and Technologies Used

- **Microsoft Azure** (Virtual Machines/Compute)
- **Remote Desktop Protocol** (RDP)
- **Internet Information Services (IIS)**
- **PHP**, **MySQL**, **osTicket**

---

## 🖥 Operating System Used

- Windows 10 Pro (21H2)

---

## ✅ Prerequisites Checklist

Before installing osTicket, ensure the following:

- [x] Internet Information Services (IIS) is installed and enabled
- [x] PHP Manager and required PHP extensions are installed
- [x] MySQL Server is installed and configured
- [x] Microsoft Visual C++ Redistributable installed
- [x] Web Platform Installer is available (optional but useful)
- [x] Permissions are configured correctly on `wwwroot` directory

---

## 🛠 Installation Steps

### 1. Install and Configure IIS
<p>
<img src="https://github.com/user-attachments/assets/c7fe9d98-4bde-498b-8712-85a01ea62e6f"


</p>

- Open **Control Panel** → **Programs and Features** → **Turn Windows features on or off**
- Enable:
  - Internet Information Services
  - CGI
  - Web Management Tools

---

### 2. Install PHP via Web Platform Installer
<p>
  <img src="https://github.com/user-attachments/assets/d85d47fc-3f07-467f-a9b0-d67551740196"


</p>

- Download **Web Platform Installer** from Microsoft
- Install **PHP 8.x** along with required extensions (IMAP, Intl, GD, etc.)
- Verify PHP is working by creating a `phpinfo.php` file in `C:\inetpub\wwwroot`

---

### 3. Install MySQL
<p>
  <img src="https://github.com/user-attachments/assets/7a6b3ba4-6ce7-4296-81e0-7737033080b2"

</p>

- Download and install **MySQL Server Community Edition**
- Create a new database and user:
  - Example:
    - Database: `osticket`
    - User: `osticketuser`
    - Password: `yourpassword`

---

### 4. Download and Configure osTicket
<p>
  <img src="https://github.com/user-attachments/assets/11632df8-fb86-45c3-a0ca-e8aa47752283"

</p>

- Download osTicket from the [official website](https://osticket.com/download/)
- Extract to `C:\inetpub\wwwroot`
- Rename `upload` folder to `osticket`
- Rename `ost-config.php` from sample and set proper permissions:
  - Grant IIS user (`IUSR` or `Everyone`) **Full Control** over `ost-config.php`

---

### 5. Complete Installation via Web Browser
- Open your browser and go to: `http://localhost/osticket`
- Fill in details like:
  - Helpdesk Name
  - Admin Email and Password
  - Database settings (use the MySQL user you created)
  

---



---

## ✅ Final Checklist

- [x] osTicket is accessible via browser
- [x] Admin dashboard is working
- [x] Emails and ticket creation are functional
- [x] Config file permissions reset for security

---

## 📄 License

This project is for educational purposes.

---

## 🙋‍♂️ Questions?

Feel free to open an issue or contact me on GitHub.

