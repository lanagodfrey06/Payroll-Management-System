# Payroll-Management-System
# Embedded Payroll Management System

## Overview

This project is an embedded payroll management system developed using an Arduino microcontroller and an LCD display interface.
The system allows payroll accounts to be created, updated, and managed through serial commands while displaying employee information on a 16x2 RGB LCD screen.

The goal of this project was to explore hardware–software integration, input validation, and data management within a constrained embedded environment.

---

## Features

* Create new payroll accounts
* Update employee job grade
* Update employee salary
* Change pension status (PEN / NPEN)
* Update employee job title
* Delete existing accounts
* Scroll through multiple employee records
* LCD display interface with colour indicators
* Serial command interface for system control

---
## 🛠 Technologies Used

- **Language:** C++ (Arduino)
- **Platform:** Arduino IDE / Arduino framework
- **Libraries:**
  - Wire
  - Adafruit_RGBLCDShield
  - Adafruit_MCP23017
- **Hardware:** Arduino microcontroller with Adafruit RGB LCD Shield

## Hardware Used

* Arduino microcontroller
* Adafruit RGB LCD Shield
* Serial communication via USB

The LCD display is used to present employee information and navigation indicators.

---

## System Behaviour

### Account Management

The system stores payroll accounts containing:

* Employee ID
* Job grade
* Job title
* Salary
* Pension status

Accounts are stored in memory and sorted automatically by employee ID.

### Display Interface

Employee information is shown on a **16x2 LCD screen**, displaying:

* Job grade
* Pension status
* Salary
* Employee ID
* Job title

Navigation arrows allow the user to scroll through accounts.

If the job title exceeds the available display width, it automatically scrolls.

### Visual Indicators

The LCD backlight colour indicates pension status:

* **Green** → Pension enrolled (PEN)
* **Red** → No pension (NPEN)

Holding the **select button** displays the student ID on the screen.

---

## Serial Commands

The system is controlled using structured serial commands.

Examples include:

ADD new employee
ADD-ID-GRADE-JOBTITLE

Update pension status
PST-ID-PEN
PST-ID-NPEN

Update salary
SAL-ID-SALARY

Update job grade
GRD-ID-GRADE

Change job title
CJT-ID-JOBTITLE

Delete employee
DEL-ID

The system includes validation checks to ensure correct input formats.

---

## Concepts Demonstrated

* Embedded systems programming
* Serial communication
* Data structures and struct usage
* Input validation and error handling
* LCD display control
* Hardware–software integration
* Memory management in constrained systems

---

## Academic Context

This project was developed as part of university coursework exploring embedded systems and hardware–software integration.

---

## Possible Improvements

Future improvements could include:

* External storage for persistent payroll data
* Keypad input instead of serial commands
* Menu-driven LCD interface
* Additional employee attributes
* Expanded display options
