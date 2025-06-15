Rock Paper Scissors GUI
🔹 Project Title:
Rock Paper Scissors GUI

🔹 Description:
This is a simple Rock Paper Scissors game implemented in Python using tkinter.
The game lets you select rock, paper, or scissors, and then it plays against a computer opponent.
The result (Win, Loss, or Tie) is displayed directly in the GUI.

🔹 Features:
✅ GUI implemented with tkinter.
✅ User-friendly and interactive.
✅ Allows you to select rock, paper, or scissors with a button click.
✅ Displays the result immediately.
✅ Purely implemented in Python, no external libraries required.

🔹 Tech Stack:
Python 3

tkinter (Python GUI framework)

random (Python's standard library)

🔹 Installation:
1️⃣ Clone this repository:

bash
Copy
Edit
git clone https://github.com/your-username/rock-paper-scissors.git
2️⃣ Navigate to directory:

bash
Copy
Edit
cd rock-paper-scissors
3️⃣ Make sure you have Python 3 installed.
You can check by:

bash
Copy
Edit
python --version
or

bash
Copy
Edit
python3 --version
🔹 How to Run:
➥ Once you’re in the directory, run:

bash
Copy
Edit
python rps_game.py
or:

bash
Copy
Edit
python3 rps_game.py
➥ The GUI should appear immediately.
➥ Select Rock, Paper, or Scissors.
➥ The computer's choice and result will be displayed on the GUI.

🔹 File Structure:
bash
Copy
Edit
rock-paper-scissors/
│
├── rps_game.py  # Main code with GUI
├── README.md    # Project Documentation
🔹 Main Code Explanation:
python
Copy
Edit
def play_game(user_choice):
    """Play the game against the computer's choice."""
    choices = ['rock', 'paper', 'scissors']
    computer_choice = random.choice(choices)

    if user_choice == computer_choice:
        result = "It\'s a tie!"
    elif (user_choice == 'rock' and computer_choice == 'scissors') or \
         (user_choice == 'paper' and computer_choice == 'rock') or \
         (user_choice == 'scissors' and computer_choice == 'paper'):
        result = "You win!"
    else:
        result = "You lose!"

    result_label.config(text=f"Your choice: {user_choice}\nComputer's choice: {computer_choice}\n{result}")
The play_game() function:

Initializes a list of choices.

The computer's choice is made by random.choice(choices).

Prints result based on conditions.

Displays result on GUI label.

🔹 GUI components:
python
Copy
Edit
root = tk.Tk()
root.title("Rock Paper Scissors")
root.geometry("400x400")
root.config(bg="#edf2f4")
Initializes main window.

Sets dimensions and background color.

python
Copy
Edit
label = tk.Label(root, text="Choose Rock, Paper, or Scissors!", font=('Helvetica', 16), bg="#edf2f4")
label.pack(pady=20)
Displays instructions at the top of the GUI.

python
Copy
Edit
frame = tk.Frame(root, bg="#edf2f4")
frame.pack()
Container to hold the 3 button widgets.

python
Copy
Edit
rock = tk.Button(frame, text="Rock", font=('Helvetica', 14), command=lambda: play_game('rock'), width=10)
paper = tk.Button(frame, text="Paper", font=('Helvetica', 14), command=lambda: play_game('paper'), width=10)
scissors = tk.Button(frame, text="Scissors", font=('Helvetica', 14), command=lambda: play_game('scissors'), width=10)

rock.grid(row=0, column=0, padx=10, pady=10)
paper.grid(row=0, column=1, padx=10, pady=10)
scissors.grid(row=0, column=2, padx=10, pady=10)
Buttons to select your move.

python
Copy
Edit
result_label = tk.Label(root, text="", font=('Helvetica', 14), bg="#edf2f4")
result_label.pack(pady=20)
Displays the result afterwards.

🔹 Possible Improvement Ideas:
➥ Scoreboard to track wins, losses, and ties.
➥ Display images instead of text for Rock, Paper, and Scissors.
➥ Animations or sounds upon choosing.

🔹 Contribution:
If you'd like to contribute:
1️⃣ Fork this repository.
2️⃣ Create a new branch:

bash
Copy
Edit
git checkout -b feature-name
3️⃣ Make your modifications.
4️⃣ Push back to your repository.
5️⃣ Submit a pull request.

🔹 License:
This project is open source under the MIT License.
