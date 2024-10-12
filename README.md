Here is the full README file as requested:

---

# AsyncTriviaEngine

## Overview
AsyncTriviaEngine is a dynamic trivia game platform designed for two players, alternating between answering trivia questions across different categories and difficulty levels. This platform supports real-time question fetching, score calculation, and intuitive UI elements to keep the game engaging and competitive.

The platform is built using HTML, CSS, and vanilla JavaScript. It does not require additional backend frameworks and is designed to be fully client-side, relying on external APIs to fetch questions dynamically.

## Features

- **Dual Player Support:** Two players can compete in answering trivia questions, with each player's turn highlighted.
- **Asynchronous Gameplay:** Real-time question fetching using [The Trivia API](https://opentdb.com/), providing a variety of question categories and difficulties (Easy, Medium, Hard).
- **Dynamic Scoring System:** Players are awarded points based on question difficulty:
  - Easy: 10 points
  - Medium: 15 points
  - Hard: 20 points
- **User-Friendly UI:** Modern, responsive interface that is accessible across various devices.
- **End-Game Results:** Displays the winner with a score comparison and an option to save the player's score.
- **Real-Time Notifications:** Includes a notification system to display game events such as the winner announcement.

## How It Works

1. **Player Setup:**
   - Players input their names on the welcome screen and start the game.
   
2. **Category Selection:**
   - The game fetches a set of trivia questions from various categories (e.g., General Knowledge, Science, History).
   
3. **Turn-based Questioning:**
   - Player 1 and Player 2 take turns answering trivia questions.
   - The current player's turn is displayed at the top of the screen.
   
4. **Scoring:**
   - Correct answers are awarded based on the difficulty of the question.
   - After 10 questions, the player with the higher score is declared the winner.

5. **Game End:**
   - Displays final scores for both players.
   - Option to restart the game or save the score.

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/SRIKANTH284/AsyncTriviaEngine.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd AsyncTriviaEngine
   ```

3. **Open the Game in Your Browser:**
   Simply open the `index.html` file in your browser:
   ```bash
   open index.html
   ```
   Or if you prefer to use a local server:
   ```bash
   npx http-server .
   ```

## Usage

1. Start by entering both player names on the landing page.
2. The game alternates between players to answer questions.
3. Points are awarded based on the difficulty of each question.
4. After 10 questions, the game will declare the winner.
5. Optionally, save your score or play again.

## Project Structure

```
AsyncTriviaEngine/
│
├── data/              # Contains JSON-based data or API fetch logic
├── pages/             # HTML files (game, end, highscore pages)
│   ├── index.html     # Welcome page
│   ├── game.html      # Game page where trivia takes place
│   ├── end.html       # End screen showing final scores
│
├── scripts/           # JavaScript logic and core game logic
│   ├── game.js        # Game logic handling turns and questions
│   ├── end.js         # Logic for handling end-game actions
│   ├── highscores.js  # Logic for displaying and saving highscores
│
├── styles/            # CSS files for styling the UI
│   ├── app.css        # Global styles and UI design
│   ├── game.css       # Styles specific to the game interface
│
└── README.md          # You are here!
```

## API Reference

This platform uses the [Open Trivia Database API](https://opentdb.com/), a free-to-use trivia question database API that provides questions from a variety of categories, difficulties, and formats.

Sample API request to fetch trivia questions:
```javascript
fetch('https://opentdb.com/api.php?amount=10&type=multiple')
  .then(response => response.json())
  .then(data => {
    // Handle question data here
  });
```

## Contributing

Contributions are welcome! Please follow the steps below to contribute:

1. Fork the repository.
2. Create a new feature branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Open a pull request.

## Future Improvements

- **Multiple Game Modes:** Adding support for more than two players or timed challenges.
- **More Customization:** Custom categories or selecting specific difficulties.
- **Leaderboard:** Global or local leaderboard to track top scores across sessions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
