# PRODIGY_CS_03 - Password Complexity Checker

## Description
A Python program that checks and evaluates the 
strength of a password based on multiple security 
criteria. The tool provides real-time feedback using 
a color-coded GUI built with Tkinter.

## Features
- 🔐 Checks password length (minimum 8 characters)
- 🔠 Detects uppercase letters (A-Z)
- 🔡 Detects lowercase letters (a-z)
- 🔢 Detects numbers (0-9)
- ✳️ Detects special characters (!@#$%...)
- 📊 Live progress bar with color-coded strength meter
- 👁️ Show/Hide password toggle button

## How It Works
- User types a password in the input field
- Tool instantly checks all 5 criteria using regex
- Progress bar fills based on score (each criteria = 20%)
- Color changes Red → Yellow → Green based on strength
- Feedback shows exactly which criteria are missing

## Code Explanation
- `re.search()` checks each criteria using regex patterns
- `check_password_strength()` evaluates password and returns score + feedback
- `update_strength()` updates GUI in real-time on every key press
- `toggle_password()` shows or hides the password text
- `ttk.Progressbar` visually represents strength percentage

## Technologies Used
- Python 3.13
- Tkinter (GUI)
- re (Regex Module)

## How to Run
- Open IDLE
- File → Open → select `task3_password_checker.py`
- Press F5 to run

## Example

### 🔴 Weak Password
- Input: `cyber`
- Score: 1/5
- Missing: Length, Uppercase, Number, Special character
- Output: 🔴 Weak Password

### 🟡 Moderate Password
- Input: `cyber123`
- Score: 4/5
- Missing: Special character
- Output: 🟡 Moderate Password

### 🟢 Strong Password
- Input: `Cyber123$`
- Score: 5/5
- Missing: Nothing ✅
- Output: 🟢 Strong Password!

