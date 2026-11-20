# CreationWebsite
# ♚ True King
 
> "A true king doesn't chase every piece. He plays for checkmate."
 
True King is a chess app for clubs and friends. Play on a 3D board, run Swiss tournaments, and climb a live ranking. It is a single HTML file with no build step and no dependencies.
 
## Features
 
### Play
- Full chess rules: check, checkmate, stalemate, castling, en passant
- Promotion picker (queen, rook, bishop, knight)
- Draw rules: threefold repetition, 50-move rule, insufficient material
- Two modes: **2 players** on one device, or **vs Computer** (Easy, Medium, Hard)
- Hint button that shows the best move
- Drag-and-drop or tap-to-move
- Board turns to face the player on move (2-player mode)
- 3D tilted board with a 2D toggle, plus six board styles
- Sound effects and move animations
- Undo, resign, flip board
### Clocks
- Presets: Blitz 3+2, Blitz 5+0, Rapid 10+0, Rapid 15+10, or no clock
- Running out of time counts as a loss
### Moves and export
- Move list with replay controls (first, previous, next, latest)
- PGN export that works with Lichess and Chess.com
### Tournament
- Swiss pairings with no repeat opponents where possible, plus byes for odd player counts
- Record results by hand, or play each pairing on the board and have the result saved automatically
- Add as many rounds as you like, with tiebreak handling and a champion banner
- Live standings with points, W/D/L and tiebreak
### Ranking (Hall of kings)
- Podium for the top three, rank titles (Pawn to King) and win/draw/loss bars
- Win = 3 points, draw = 1, defeat = 0, and a 🏆 for each tournament won
- Updates automatically from tournaments and casual games; names can be removed
- **New tournament** clears players, matches and the ranking
## Run it
 
No install needed.
 
1. Download or clone this repo.
2. Open `index.html` in any modern browser.
```bash
git clone https://github.com/RohithKumar6/CreationWebsite.git
cd CreationWebsite
# open index.html in your browser
```
 
## Deploy with GitHub Pages
 
1. Push the repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Your site appears at `https://<your-username>.github.io/CreationWebsite/`.
## Project structure
 
```
CreationWebsite/
├── index.html       # the whole app (HTML, CSS, JavaScript)
├── README.md
├── screenshot.png   # optional
└── LICENSE
```
 
## How it works
 
- **Engine:** a board stored as a 64-square array, legal-move generation, and a small minimax search with alpha-beta pruning for the computer.
- **Difficulty:** Easy plays partly at random, Medium looks 2 moves ahead, Hard looks 3.
- **Storage:** tournament data, rankings and board style are saved in the browser's `localStorage`. Nothing is sent to a server.
- **Styling:** plain CSS with light and dark themes and CSS 3D transforms for the board.
## Known limitations
 
- Data is stored per browser, so rankings are not shared between devices.
- The computer always promotes to a queen.
- The 3D board is a CSS tilt, not a WebGL scene.
- Tiebreak rounds use the normal Swiss pairing, not a match between only the tied leaders.
## Roadmap
 
- [ ] Automated tests for move generation (perft) and pairing logic
- [ ] Accounts and a shared database so rankings work across devices
- [ ] Shareable live standings link
- [ ] Lichess integration (import ratings by username)
- [ ] Round-robin and knockout formats
- [ ] Daily puzzles and achievements
- [ ] Full WebGL 3D board with a rotatable camera
## Contributing
 
Issues and pull requests are welcome. For larger changes, please open an issue first to discuss what you would like to change.
 
## License
 
[MIT](LICENSE)
 
## Author
 
Built by **Pasupuleti Rohith Kumar** · [GitHub](https://github.com/RohithKumar6)
 
