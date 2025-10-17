# 1) Create & activate a virtual env
python -m venv .venv
# Windows
.\.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# 2) Install deps
pip install -r requirements.txt

# 3) Start the app (creates app.db on first run)
flask --app app run --debug
# course-registration-system
A Python Program that allows students to register for and manage courses using OOP principles.
