# Shaiya Asgard - Website - 2025

![GitHub repo size](https://img.shields.io/github/repo-size/matheusvalpassos/ShaiyaAsgardV2?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/matheusvalpassos/ShaiyaAsgardV2?style=for-the-badge)

<img src="imagem.png" alt="Example image">

> This is a modern website project for the game Shaiya Asgard, developed with Django. It offers user authentication, a new interface design (UI/UX), and a dynamic ranking system integrated with a relational database.

### Adjustments and Improvements

The project is still under development, and future updates will focus on the following tasks:

- [x] Implementation of user authentication (registration and login).
- [x] Development of a new UI/UX design for the website.
- [x] Addition of a ranking table linked to the database.
- [ ] Creation of a user control panel.
- [ ] Performance and security optimization.
- [ ] Addition of news and events features.

Before you begin, make sure you meet the following requirements:

- You have installed the latest version of Python 3.10+ (required for Django 5.1.6).
- You have pip installed and updated.
- You have Node.js and npm installed (required to compile Tailwind CSS).
- You have SQL Server installed or access to a SQL Server instance for the database.
- ODBC Driver for SQL Server: To connect to MSSQL, it is crucial that you have the corresponding ODBC driver installed on your system (e.g., ODBC Driver 17 for SQL Server).
- You have a Windows machine for the production setup (Windows Server and Nginx). The development environment is compatible with Windows, Linux, and macOS.
- You have read the installation and configuration sections below.

## Installing Shaiya Asgard Website

To install and configure the Shaiya Asgard Website, follow these steps:

### 1. Clone the repository:

bash
git clone https://github.com/matheusvalpassos/Shaiya-Django-Website.git
cd Shaiya-Django-Website
### 2. Create and activate the virtual environment:

Linux e macOS:
```
python3 -m venv .venv
source .venv/bin/activate
```

Windows:
```
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install Python dependencies:

All dependencies listed in requirements.txt will be installed.
```
pip install -r requirements.txt
```

### 4. Install Node.js dependencies (for Tailwind CSS):
```
npm install
```

### 5. Configure the database connection (MSSQL):

Edit the myproject/settings.py file (or wherever your DB settings are, such as config/settings.py) and configure the DATABASES section to point to your SQL Server. Example:

# myproject/settings.py (or config/settings.py)
```
DATABASES = {
'default': {
'ENGINE': 'mssql', # Or 'sql_server.pyodbc' depending on your configuration
'NAME': 'YOUR_DATABASE',
'HOST': 'YOUR_SQL_SERVER',
'PORT': '', # Leave blank for the default port (1433)
'USER': 'YOUR_DB_USER',
'PASSWORD': 'YOUR_DB_PASSWORD',
'OPTIONS': {
'driver': 'ODBC Driver 17 for SQL Server', # Verify the correct ODBC driver is installed
'autocommit': True, # Optional: for automatic commits after each operation
},
}
}
```
⚠️ Make sure you have the ODBC driver correctly installed on your system!

### 6. Run database migrations:

```python manage.py migrate```

### 7. Compile Tailwind CSS:

```npm run build-tailwind```

# Or the command you configured to compile the CSS

(If you configured npx tailwindcss -i ./src/input.css -o ./static/css/main.css --watch in package.json, this could be npm run watch-tailwind for development or npm run build-tailwind for production.)

## ☕ Using the Shaiya Asgard Website

Start the development server:

```
python manage.py runserver
```

Acesse: http://127.0.0.1:8000/ non-browser.

### Available Features:

**Home Page**: Project presentation with interactive visuals.

**Authentication**: Register or log in with dynamic forms.

**Ranking**: View the leaderboard integrated with the database.

## 📫 Contributing to the Project

To contribute to the Shaiya Asgard Website, follow the steps outlined in the contributing guide:

1. Fork this repository.
2. Create a branch: `git checkout -b <branch_name>`.
3. Make your changes and commit them: `git commit -m '<commit_message>``.
4. Push to the original branch: `git push origin <project_name> / <location>`.
5. Create the pull request.

Alternatively, see the GitHub documentation at [Contributing Guide (CONTRIBUTING.md)](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## 🤝 Contributors

Thank you to the following people who helped with this project:

<table>
<tr>
<td align="center">
<a href="https://github.com/matheusvalpassos" title="Matheus Valpassos">
<img src="https://avatars.githubusercontent.com/matheusvalpassos" width="100px" alt="Matheus's Photo"/><br>
<sub><b>Matheus Valpassos</b></sub>
</a>
</td>
</tr>
</table>

## 😄 Become a Contributor

Want to be part of this project? Click [HERE](CONTRIBUTING.md) and read how to contribute.

## 📝 License

This project is licensed. See the [LICENSE.md] file for more details.
