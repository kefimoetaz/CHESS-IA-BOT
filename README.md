# Chess Game with AI Opponent ♟️

A fully functional chess game built in Python with Tkinter GUI, featuring strategic AI opponent and complete chess rule implementation.

![Python](https://img.shields.io/badge/python-v3.6+-blue.svg)
![Tkinter](https://img.shields.io/badge/GUI-Tkinter-green.svg)
![PIL](https://img.shields.io/badge/Images-PIL-orange.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🎯 Features

### Core Gameplay
- ✅ **Complete chess implementation** with all standard rules
- ✅ **Turn-based gameplay** (White vs Black)
- ✅ **Legal move validation** for all piece types
- ✅ **Check and checkmate detection**
- ✅ **Castling support** (kingside and queenside)
- ✅ **Pawn promotion** with piece selection menu
- ✅ **King capture prevention** (proper chess rules)

### AI Opponent
- 🤖 **Strategic AI bot** playing as Black
- 🧠 **Move evaluation system** prioritizing:
  - Capturing valuable pieces (Queen=9, Rook=5, Bishop/Knight=3, Pawn=1)
  - Controlling center squares (d4, d5, e4, e5)
  - Advancing pieces toward opponent
- ⚡ **Check response** - AI must escape check when threatened
- 👑 **Automatic pawn promotion** to Queen

### User Interface
- 🎨 **Visual 8x8 chessboard** with alternating colors
- 🖼️ **Custom piece graphics** (PNG images)
- 🖱️ **Click-to-move interface** (select piece → select destination)
- 🎯 **Visual feedback** with square highlighting

## 🚀 Quick Start

### Prerequisites
```bash
pip install pillow
```

### Installation
1. **Clone the repository**
```bash
git clone https://github.com/yourusername/chess-game.git
cd chess-game
```

2. **Run the game**
```bash
python chess.py
```

## 📁 Project Structure
```
chess-game/
├── chess.py          # Main game logic and GUI
├── white/            # White piece images
│   ├── k.png        # King
│   ├── q.png        # Queen
│   ├── r.png        # Rook
│   ├── b.png        # Bishop
│   ├── n.png        # Knight
│   ├── p.png        # Pawn
│   └── blank.png    # Empty square
├── black/           # Black piece images (same structure)
└── README.md
```

## 🎮 How to Play

1. **Start the game** - White pieces move first
2. **Make a move** - Click your piece, then click destination square
3. **AI responds** - Black AI automatically makes its move
4. **Win condition** - Checkmate the opponent's king

### Controls
- **Left click** - Select piece or destination
- **Invalid moves** - Automatically rejected
- **Turn enforcement** - Can only move your own pieces

## 🛠️ Technical Implementation

### Architecture
- **Object-Oriented Design** - Main `Board` class handles all logic
- **Event-Driven GUI** - Tkinter button callbacks for user interaction
- **Modular Functions** - Separate methods for move validation, AI logic, etc.

### Key Components
```python
class Board(tk.Frame):
    def select_piece()        # Handle player moves
    def allowed_piece_move()  # Validate piece movements
    def in_check()           # Detect check conditions
    def bot_move()           # AI decision making
    def get_simple_moves()   # Generate legal moves
```

### AI Algorithm
1. **Generate all legal moves** for current position
2. **Evaluate each move** using scoring system:
   - Material gain (captured pieces)
   - Positional advantage (center control)
   - Forward progress
3. **Select best move** from highest-scoring options
4. **Execute move** and update game state

## 🔧 Technologies Used

- **Python 3.6+** - Core programming language
- **Tkinter** - GUI framework (built-in with Python)
- **PIL/Pillow** - Image processing for piece graphics
- **Object-Oriented Programming** - Clean, maintainable code structure

## 🎯 Chess Rules Implemented

### Piece Movements
- **Pawn** - Forward movement, diagonal capture, 2-square initial move
- **Rook** - Horizontal and vertical movement
- **Knight** - L-shaped movement (can jump over pieces)
- **Bishop** - Diagonal movement
- **Queen** - Combination of rook and bishop
- **King** - One square in any direction

### Special Rules
- **Castling** - King and rook special move
- **Pawn Promotion** - Promote to Queen, Rook, Bishop, or Knight
- **Check Detection** - King under attack
- **Checkmate** - King in check with no legal moves
- **Stalemate** - No legal moves but king not in check

## 🚧 Future Enhancements

- [ ] **En passant** capture implementation
- [ ] **Move history** and undo functionality
- [ ] **Save/Load game** feature
- [ ] **Difficulty levels** for AI
- [ ] **Multiplayer support** over network
- [ ] **Opening book** for AI
- [ ] **Move timer** and clock
- [ ] **Game analysis** and move suggestions

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/kefimoetaz)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/kefimoetaz)

## 🙏 Acknowledgments

- Chess piece images from open source collections
- Inspiration from classic chess implementations
- Python community for excellent documentation

---


⭐ **Star this repository if you found it helpful!**
