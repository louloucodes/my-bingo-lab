```instructions
---
name: workspace
description: Workspace-specific setup, architecture, and development guidelines for the Soc Ops bingo game project.
---

# Soc Ops Workspace Instructions

## Development Checklist
Before committing changes, ensure:
- [ ] `npm run lint` passes (no errors)
- [ ] `npm run build` succeeds (production build)
- [ ] `npm run test` passes (all 21 tests)

## Project Overview

**Soc Ops** is a React 19 + TypeScript social bingo game for in-person mixers. Players find people matching descriptions to achieve 5-in-a-row wins.

**Tech Stack**: Vite 7, Tailwind CSS v4, Vitest, ESLint, GitHub Pages deployment

## Quick Start

```bash
npm install          # Install dependencies
npm run dev          # Start dev server (localhost:5173)
npm run lint         # Check code quality
npm run test         # Run tests
npm run build        # Production build
```

## Project Structure

```
src/
├── components/       # BingoBoard, BingoSquare, GameScreen, StartScreen
├── hooks/
│   └── useBingoGame.ts     # Game state management
├── utils/
│   ├── bingoLogic.ts       # Core algorithms (board, win detection)
│   └── bingoLogic.test.ts  # 21 passing tests
├── data/
│   └── questions.ts        # Question pool
├── types/
│   └── index.ts            # TypeScript definitions
├── App.tsx, main.tsx, index.css
public/, .lab/, .github/instructions/
```

## Core Architecture

### Game Logic (`src/utils/bingoLogic.ts`)
- `generateBoard()` — Creates 25-square board with 24 random questions + free center
- `toggleSquare(board, index)` — Mark/unmark squares (immutable updates)
- `checkBingo(board)` — Detect 5-in-a-row (rows, columns, diagonals)
- `getWinningSquareIds(board, winType)` — Identify winning squares

### State Management (`src/hooks/useBingoGame.ts`)
- Manages board state, player interactions, win detection
- Consumed by `GameScreen.tsx`

### Components
- **BingoBoard** — 5×5 grid rendering
- **BingoSquare** — Individual square with question and toggle
- **GameScreen** — Active game state
- **StartScreen** — Initial state
- **BingoModal** — Win announcement

## Development Guidelines

### Code Standards
- **TypeScript**: Strict mode enabled; use type annotations
- **Components**: Functional only; define `Props` interfaces above component
- **Immutability**: Always create new arrays/objects, never mutate state
- **Styling**: Tailwind v4 utilities + global CSS in `index.css`
- **Testing**: Unit tests in `*.test.ts` files; test behavior not implementation

### Git Workflow
- **main**: Production code, auto-deploys to GitHub Pages
- **feature/\***: Feature branches
- **Commit often** with descriptive messages
- **Test before pushing**: Run full lint + build + test suite

### Customization

**Add Questions**: Edit `src/data/questions.ts`

**Adjust Game Rules**: Modify `src/utils/bingoLogic.ts`:
- Board size: `generateBoard()`
- Win conditions: `checkBingo()`

**Theme & Styling**: Update `index.css` and component classes

## Troubleshooting

```bash
# Clear and reinstall
rm -rf node_modules package-lock.json && npm install

# TypeScript errors
npx tsc --noEmit

# Lint issues
npm run lint -- --fix
```

## Key Files Reference

| File | Purpose |
|------|---------|
| `src/utils/bingoLogic.ts` | Game algorithms |
| `src/hooks/useBingoGame.ts` | Game state |
| `src/components/BingoBoard.tsx` | Board rendering |
| `src/data/questions.ts` | Question pool |
| `src/index.css` | Global styles |

## Resources for AI Agents
- Read `.lab/GUIDE.md` for workshop context
- Refer to `frontend-design.instructions.md` for UI design
- Refer to `tailwind-4.instructions.md` for CSS patterns
```
