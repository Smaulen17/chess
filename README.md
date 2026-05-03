# ♟️ Chess Web App

Это веб-приложение для игры в шахматы в браузере. Проект создан с целью практики фронтенд-разработки и работы с игровыми движками.

## 🚀 Функционал

- Игра в шахматы против компьютера
- Поддержка Stockfish движка
- Подсветка возможных ходов
- Проверка шаха и мата
- Возможность играть с другим игроком (если добавлено)
- Адаптивный интерфейс

## 🧠 Технологии

- HTML5
- CSS3
- Node.js 
- Stockfish.js (шахматный движок)
- WebAssembly (WASM)

## 📂 Структура проекта
gameStore
├── chess          — chess.js Chess instance (move validation, FEN, PGN)
├── status         — 'idle' | 'playing' | 'check' | 'checkmate' | 'stalemate' | 'draw'
├── playerColor    — 'w' | 'b'
├── mode           — 'ai' | 'analysis'
├── whiteTime      — seconds remaining for white
├── blackTime      — seconds remaining for black
├── activeTimer    — which clock is ticking
├── initGame()     — sets up a new game from a GameConfig object
├── makeMove()     — validates + applies a move, updates status, switches timer
├── startTimer()   — begins the countdown loop
└── resetGame()    — clears everything back to idle
