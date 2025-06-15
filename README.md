# mittasks
🔹 Project Title:
Simple GUI Calculator in Python (using Tkinter)

🔹 Description:
This is a simple GUI calculator application implemented in Python using the Tkinter library.
It performs basic mathematical operations — addition (+), subtraction (−), multiplication (×), division (/), and decimal — through a graphical interface.
The application lets you:

Perform calculations by clicking on button widgets.

Display the result directly on the GUI.

Clear the display when needed.

🔹 Features:
✅ Graphical User Interface:
Provides a simple and interactive GUI for all operations.

✅ Basic Operations:
Addition, subtraction, multiplication, division.

✅ Clear Button:
Clears the display for a new expression.

✅ Error Handling:
Displays “Error” if an invalid expression is entered (like division by zero).

🔹 Tech Stack:
Language: Python 3.x

Framework: Tkinter (Python's standard GUI toolkit)

🔹 File: calculator.py
python
Copy
Edit
import tkinter as tk

def button_click(item):
    """Add number or operator to the display."""
    current = entry.get()
    entry.delete(0, tk.END)
    entry.insert(0, current + item)

def clear():
    """Clear the display."""
    entry.delete(0, tk.END)

def calculate():
    """Evaluate the expression in the display."""
    expression = entry.get()
    try:
        result = eval(expression)  # eval parses and executes the expression safely here
        entry.delete(0, tk.END)
        entry.insert(0, result)
    except Exception as e:
        entry.delete(0, tk.END)
        entry.insert(0, "Error")

# Create main window
root = tk.Tk()
root.title("Simple Calculator")
root.geometry("350x400")
root.resizable(False, False)

# Display widget
entry = tk.Entry(root, font=('arial', 18), borderwidth=5, relief='solid')
entry.grid(row=0, column=0, columnspan=4, ipadx=8, ipady=8)

# Buttons
buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    '0', '.', '=', '+',
    'C'
]

row_val = 1
col_val = 0

for button in buttons:
    if button == "=":
        cmd = calculate
    elif button == "C":
        cmd = clear
    else:
        cmd = lambda x=button: button_click(x)

    button = tk.Button(root, text=button, font=('arial', 18),
                       width=4, height=1, command=cmd)
    button.grid(row=row_val, column=col_val, padx=5, pady=5)

    col_val += 1
    if col_val > 3:
        col_val = 0
        row_val += 1

root.mainloop()
🔹 Installation:
✅ Requirements:
Python 3.x installed on your computer.
(No additional libraries needed; tkinter comes bundled with Python).

🔹 How to Run:
1️⃣ Download or clone this repository.

2️⃣ Open cmd or terminal in the directory where calculator.py is located.

3️⃣ Run the following command:

bash
Copy
Edit
python calculator.py
4️⃣ The GUI should appear immediately.

🔹 How to Use:
➥ Click on the number or operator you want to use.
➥ The expression will appear on the display.
➥ To compute the result, click “=”.
➥ To clear the display, click “C”.
➥ To close the application, simply close the GUI window.

🔹 Possible Enhangements:
✅ Support for more operations (square roots, exponents, percentages).

✅ Handle brackets for complex expressions.

✅ Handle keyboard input alongside mouse clicks.

✅ Provide a history of previous calculations.

🔹 Summary:
This simple GUI calculator is a perfect beginner-friendly Python project.
It demonstrates:

GUI fundamentals with Tkinter

event handling

use of eval() to compute mathematical expressions

designing a GUI application from scratch

coding structures like functions, loops, try/except

✅ Author:
[micro IT internship]
[Internship Project, 2025]

