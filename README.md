# Social-Media-Dashboard-Using-Django

SOCIAL MEDIA DASHBOARD USING DJANGO 📌 PROBLEM STATEMENT Social media users struggle to manage multiple platforms efficiently. This project aims to build a Django-based Social Media Dashboard that aggregates posts, comments, and user activity from various platforms into a single, unified interface.

🎯 OBJECTIVE The goal is to create an interactive, secure, and scalable dashboard that allows users to: ✔ Authenticate & Manage Profiles (Signup, login, integrate social media accounts) ✔ Fetch & Display Social Media Data (Posts, comments, likes) ✔ Enable User Interaction (Like, comment, share posts) ✔ Post & Schedule Updates (Directly from the dashboard) ✔ Provide Analytics & Engagement Insights ✔ Ensure Security & Error Handling

🛠️ PREREQUISITES Before setting up the project, ensure you have the following installed:

✔ Python 3.x ✔ Django ✔ Virtual Environment (venv) ✔ Facebook & Twitter API Credentials ✔ Redis & Celery (for scheduled posting, if enabled)

⚙️ TECHNOLOGIES USED ✔ Backend: Django, Django REST Framework ✔ Frontend: HTML, CSS (Bootstrap/Tailwind CSS) ✔ Database: SQLite / PostgreSQL ✔ APIs: Facebook Graph API, Twitter API ✔ Authentication: OAuth (social-auth-app-django) ✔ Task Scheduling: Celery & Redis ✔ Deployment: Heroku / AWS / Any cloud platform (optional)

🚀 PROJECT SETUP 1️⃣ INSTALL DEPENDENCIES 2️⃣ CONFIGURE ENVIRONMENT VARIABLES 3️⃣ RUN DATABASE MIGRATIONS 4️⃣ CREATE SUPERUSER (FOR ADMIN PANEL) 5️⃣ RUN THE DJANGO PROJECT

🌟 FEATURES IMPLEMENTED 🔹 USER AUTHENTICATION & PROFILE MANAGEMENT ✔ Users can sign up, log in, and manage their profiles. ✔ OAuth authentication for Facebook & Twitter.

🔹 SOCIAL MEDIA INTEGRATION ✔ Fetch posts, comments, and likes from Facebook & Twitter. ✔ Post updates and schedule posts from the dashboard.

🔹 DASHBOARD UI & USER EXPERIENCE ✔ Interactive & Responsive UI with Bootstrap/Tailwind CSS. ✔ Easy navigation for viewing and managing social media activities.

🔹 ENGAGEMENT ANALYTICS ✔ User engagement insights (most liked posts, comments trends). ✔ Dashboard visualization for social media performance.

🔹 SECURITY & ERROR HANDLING ✔ Secure API authentication for social media integrations. ✔ Proper error messages for failed API calls and user actions.

📌 OPTIONAL FEATURES ✔ Scheduled Posting (Celery + Redis for automated posts). ✔ Multi-platform Posting (Post on all linked accounts simultaneously). ✔ Advanced Analytics (Heatmaps, engagement trends).

📊 IMPACT & BENEFITS ✔ Time-Saving: No need to log in to multiple platforms separately. ✔ Improved Engagement: Post and interact from a unified interface. ✔ Data-Driven Decisions: Gain insights from analytics. ✔ Scalability: Can be extended to support more platforms like Instagram, LinkedIn.

📌 FUTURE ENHANCEMENTS 🔹 Integrate more social media platforms (Instagram, LinkedIn). 🔹 Implement AI-based analytics for engagement prediction. 🔹 Add customizable notifications for user activities.

📜 CONCLUSION The Social Media Dashboard using Django provides a centralized, efficient, and user-friendly way to manage social media activities. By integrating authentication, interaction, analytics, and scheduling, this project offers a comprehensive solution for users who need better control over their digital presence.

📎 AUTHOR Satyam Gupta.

STEP BY TSEP INSTRUCTION TO RUN THE CODE TO SEE OUTPUT.

I inspected the zip you uploaded. Quick summary first (so you can copy-paste exact commands):

manage.py is located at: Social-Media-Dashboard-Django-main/manage.py

requirements.txt is located at: Social-Media-Dashboard-Django-main/requirements.txt

The Django settings use SQLite (so no external DB needed) and default secret key/env fallbacks — you can run it locally without extra env vars.

Below are step-by-step terminal commands you can run. I give both Mac / Linux and Windows (PowerShell) variants. Copy the block that matches your OS.

-- Steps to run the project locally

1) Unzip and go to project folder
Mac / Linux [Copy & Paste to Terminal]
from the folder where the zip is located
unzip "1. Social-Media-Dashboard-Django-main.zip" cd "Social-Media-Dashboard-Django-main" ls -la

Windows (PowerShell) [Copy & Paste To the PowerShell]
from the folder where the zip is located
Expand-Archive -LiteralPath "1. Social-Media-Dashboard-Django-main.zip" -DestinationPath "Social-Media-Dashboard-Django-main" Set-Location .\Social-Media-Dashboard-Django-main
Get-ChildItem (You should now see manage.py in the directory.)

2) Create & activate a virtual environment
Mac / Linux [Copy & Paste to Cmd Or VScode Terminal]
python3 -m venv venv source venv/bin/activate python -V # verify Python version pip install --upgrade pip setuptools wheel

Windows (PowerShell) [Copy & Paste to MS Powershell & VScode Terminal]
py -3 -m venv venv .\venv\Scripts\Activate python -V # verify Python version pip install --upgrade pip setuptools wheel

3) Install Python dependencies
Copy & Paste to VScode Terminal but having in these folder
pip install -r requirements.txt (This will install Django and other libs listed in requirements.txt.)

4) Apply database migrations
Copy & Paste to VScode Terminal
python manage.py migrate

5) (Optional) Create an admin user
Copy Or Paste to VScode Terminal.
python manage.py createsuperuser

follow prompts to set username/email/password
6) Run the development server
-- Copy Or Paste to VScode Terminal.

python manage.py runserver

Open your browser at: [Copy Or Paste to VScode Terminal.]
http://127.0.0.1:8000/ If you need to bind to all interfaces (e.g. to view from another device):

Copy Or Paste to VScode Terminal.
python manage.py runserver 0.0.0.0:8000

Quick troubleshooting tips
"No module named django" → make sure the virtualenv is activated and pip install -r requirements.txt succeeded.
If pip install errors on packages like cryptography:
First run pip install --upgrade pip setuptools wheel.

On Debian/Ubuntu you may need: sudo apt-get install build-essential libssl-dev libffi-dev python3-dev (and sometimes cargo for recent cryptography builds).

If manage.py not found → double-check you're in the Social-Media-Dashboard-Django-main folder (the file we found is at Social-Media-Dashboard-Django-main/manage.py).

Env vars: the project reads DJANGO_SECRET_KEY, DJANGO_DEBUG, DJANGO_ALLOWED_HOSTS but has defaults. To set them:
Linux/mac:
Copy Or Paste to Terminal.
export DJANGO_SECRET_KEY='mysecret' export DJANGO_DEBUG='False' export DJANGO_ALLOWED_HOSTS='localhost,127.0.0.1' Windows PowerShell:

Powershell
Copy Or Paste to PowerShell Terminal.
$env:DJANGO_SECRET_KEY='mysecret' $env:DJANGO_DEBUG='False' $env:DJANGO_ALLOWED_HOSTS='localhost,127.0.0.1'

One-line “run” summary (Mac/Linux)
Copy & Paste to Terminal
unzip "1. Social-Media-Dashboard-Django-main.zip" && cd "Social-Media-Dashboard-Django-main" && python3 -m venv venv && source venv/bin/activate && pip install --upgrade pip setuptools wheel && pip install -r requirements.txt && python manage.py migrate && python manage.py runserver

One-line “run” summary (Windows PowerShell)
Copy Or Paste to Powershell Terminal.
Expand-Archive -LiteralPath "1. Social-Media-Dashboard-Django-main.zip" -DestinationPath "Social-Media-Dashboard-Django-main"; Set-Location .\Social-Media-Dashboard-Django-main; py -3 -m venv venv; .\venv\Scripts\Activate; pip install --upgrade pip setuptools wheel; pip install -r requirements.txt; python manage.py migrate; python manage.py runserver

🚀 Happy Coding! 😊
