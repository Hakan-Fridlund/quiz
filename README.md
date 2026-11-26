# Python Quiz Application

A command-line quiz application built in Python, featuring both multiple-choice and open-ended questions. The application supports randomized question selection, category filtering, an admin menu, persistent data storage, and a high-score system.

## Features

### Quiz functionality

- **Multiple question types:** Supports both multiple-choice and open-ended questions.
- **Randomized questions:** Questions are shuffled before each quiz.
- **Category selection:** Choose between Mathematics, Nature, Geography, or a mixed quiz.
- **Custom quiz length:** Select how many questions you want to answer.
- **Case-insensitive answers:** Answers are not affected by letter casing.
- **Replay option:** Restart the quiz after completing a round.
- **Input validation:** Validates user input throughout the application to handle unexpected or invalid entries.

### Admin functionality

- **Hidden admin menu:** Access the admin menu by entering `Admin` as the username and providing the correct password (default: admin123).
- **Question management:** Add, display, and remove questions.
- **High-score management:** View the current high-score list.
- **Persistent question storage:** Save questions to a Pickle (`.pkl`) file and load them when the application starts.

### High-score system

- Saves high scores to a JSON (`.json`) file.
- Loads previously saved scores on startup.
- Displays the top five scores after completing a quiz.
- Automatically removes the lowest score when the leaderboard is full and a new qualifying score is added.

### Command-line arguments

Uses Python's `argparse` module to allow users to provide their name directly when launching the application.

To access the admin menu, enter `Admin` as the name.

Examples:

```bash
python quiz.py --name "Alex"
python quiz.py --name "Admin"
```

Alternatively, the application prompts the user for their name if no command-line argument is provided.

## Technical Implementation

The project was developed with a focus on object-oriented programming, defensive coding, file handling, and maintainability.

Key concepts and techniques used:

- **Object-oriented programming (OOP):** Uses classes, constructors, class methods, and instance methods to organize the application.
- **Inheritance and subclasses:** Specialized question classes inherit from a common `Question` base class, allowing different question types to share common functionality while implementing their own behavior.
- **Defensive programming:** Validates user input throughout the application and handles invalid entries and file-related errors to reduce the risk of unexpected behavior.
- **File handling:** Uses JSON and Pickle to save and load persistent application data.
- **Command-line interface:** Uses `argparse` to handle command-line arguments.
- **Exception handling:** Handles potential file errors and other runtime exceptions.
- **Data structures:** Uses lists, dictionaries, tuples, and list comprehensions.
- **Control flow:** Uses loops, conditional statements, and pattern matching with `match/case`.

## What I Learned

Through this project, I gained practical experience in several important areas of Python programming:

- Designing an object-oriented application using classes, inheritance, and specialized subclasses.
- Writing defensive code by validating user input and anticipating potential errors throughout the application.
- Working with file handling and persistent data storage using both JSON and Pickle.
- Structuring application logic to make the code easier to maintain and extend.
- Using command-line arguments with `argparse`.
- Applying exception handling to manage unexpected situations and file-related errors.

## Technologies

- Python 3
- Standard Python libraries:
  - `random`
  - `json`
  - `pickle`
  - `argparse`

## Running the Application

1. Clone the repository:

```bash
git clone https://github.com/Hakan-Fridlund/quiz.git
```

2. Navigate to the project directory:

```bash
cd quiz
```

3. Run the application:

```bash
python quiz.py
```

## Data Storage and Security

The application uses two file formats for persistent storage:

- **JSON (`quiz_highscore.json`):** Stores high scores in a human-readable format.
- **Pickle (`quiz_questions.pkl`):** Stores quiz questions using Python's object serialization.

**Important:** The Pickle file is a binary data file and is not intended to be opened or edited in a text editor. Doing so will not display the data in a useful format, and saving changes from a text editor may corrupt the file. The application should handle this file through Python's Pickle functionality.

Only load Pickle files from trusted sources. Loading an untrusted Pickle file can execute malicious code.

## Project Background

This project started as an assignment to create a basic quiz application and was subsequently expanded with additional functionality.

The original requirements were extended with administrative features, persistent data storage, a high-score system, command-line argument handling, and a more structured object-oriented design.

The main goal was to apply and deepen my understanding of Python programming concepts while developing a more complete, maintainable, and interactive command-line application.
