# Student Course Registration System
# Author: Niya Dawson
# Description: A simple console-based system that allows students to add, drop, and view courses.

class Student:
def __init__(self, name, student_id):
self.name = name
self.student_id = student_id
self.courses = []

def add_course(self, course):
if course not in self.courses:
self.courses.append(course)
print(f"{course} added successfully!")
else:
print(f"{course} is already registered.")

def drop_course(self, course):
if course in self.courses:
self.courses.remove(course)
print(f"{course} dropped successfully!")
else:
print(f"{course} not found in your schedule.")

def view_courses(self):
if self.courses:
print(f"\n{self.name}'s Registered Courses:")
for course in self.courses:
print(f"- {course}")
else:
print("No courses registered yet.")


# --- Main Program ---
def main():
print("Welcome to the Student Course Registration System!")
name = input("Enter your name: ")
student_id = input("Enter your student ID: ")

student = Student(name, student_id)

while True:
print("\nSelect an option:")
print("1. Add Course")
print("2. Drop Course")
print("3. View Courses")
print("4. Exit")

choice = input("Enter your choice (1-4): ")

if choice == "1":
course = input("Enter course name to add: ")
student.add_course(course)
elif choice == "2":
course = input("Enter course name to drop: ")
student.drop_course(course)
elif choice == "3":
student.view_courses()
elif choice == "4":
print("Thank you for using the system. Goodbye!")
break
else:
print("Invalid choice. Please try again.")

if __name__ == "__main__":
main()
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
