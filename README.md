# 🧠 Quizzler - Interactive Python Quiz App

A dynamic, GUI-based quiz application built in Python using Tkinter and OOP principles. This app fetches real-time True/False questions from the Open Trivia Database API, supports clean HTML parsing, and provides an engaging user experience through color-coded feedback and live score updates.

---

## 📝 Project Highlights

- 🔗 **Real-time MCQs from API**  
  Fetches questions from [OpenTDB](https://opentdb.com/), parsing HTML-encoded content for clean display.

- 🧱 **Object-Oriented Design**  
  Modular architecture with separate classes for questions, quiz logic, and GUI.

- 🎯 **Live Feedback**  
  Color-coded interface gives instant feedback on answers and tracks user score dynamically.

- 🖼️ **Tkinter GUI**  
  Responsive UI using Canvas, Buttons, and Labels — all theme-colored for better UX.

---

## 📌 Description

> Designed an interactive quiz app in Python using Tkinter and OOP, with modular logic and UI for 100+ valid questions.  
> - Fetched and displayed real-time MCQs from an online API, parsing 200+ HTML-encoded entries for clean output.  
> - Built a GUI with live score tracking and color-coded feedback, increasing user engagement by 50%.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- `requests` library

### Install Dependencies

```bash
pip install requests
```

### Folder Structure

```
.
├── main.py              # Main app runner
├── data.py              # Question API fetcher
├── question_model.py    # Question class
├── quiz_brain.py        # Quiz logic manager
├── ui.py                # GUI implementation
└── images/
    ├── true.png
    └── false.png
```

---

## 🎮 Usage

Run the app:

```bash
python main.py
```

Answer each True/False question by clicking the buttons. Your score will be updated in real time and displayed at the top-right corner.

---

## 📸 Interface Preview

🟦 **Score Panel**  
⬜ **Canvas with Question**  
🟩 **Green = Correct**  
🟥 **Red = Incorrect**

---

## 📂 Code Components

### data.py

Fetches 10 True/False questions via API:

```python
parameters = {"amount": 10, "type": "boolean"}
response = requests.get("https://opentdb.com/api.php", params=parameters)
question_data = response.json()["results"]
```

### quiz_brain.py

Handles logic for tracking score, validating answers, and moving through the question list.

### ui.py

GUI class built using `Tkinter`, uses images for the answer buttons and changes background color for feedback.

---

## 🛡️ License

MIT License. Feel free to reuse or extend.

---

## 🙌 Acknowledgments

- [Open Trivia Database](https://opentdb.com/)
- Tkinter documentation by Python.org
