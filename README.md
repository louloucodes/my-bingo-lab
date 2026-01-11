# 🎲 Soc Ops

### Break the ice. Make connections. Win at socializing.

**Soc Ops** is an interactive social bingo game designed to turn awkward mixers into engaging conversations. Perfect for conferences, team events, workshops, or any gathering where people need an excuse to talk to strangers.

---

## ✨ What Makes It Special

- 🎯 **Instant Connection** — Every square is a conversation starter
- 🎮 **Real-Time Gameplay** — Find people matching descriptions, mark your board, win with 5-in-a-row
- 🎨 **Beautiful Design** — Built with React 19 + Tailwind CSS v4 for a smooth, modern experience
- ⚡ **Zero Setup** — No accounts, no downloads. Just open and play
- 🛠️ **Fully Customizable** — Easily adapt questions for your event, team, or community

## 🎲 How to Play

1. **Open the game** on your phone or laptop
2. **Read the squares** — each contains a trait or fact (e.g., "has a pet", "speaks 3+ languages")
3. **Find people** who match the descriptions
4. **Mark squares** as you make connections
5. **Get 5 in a row** (horizontal, vertical, or diagonal) to win! 🏆

The center square is always free — start there and work your way out.

---

## 🚀 Quick Start

### Prerequisites

- [Node.js 22+](https://nodejs.org/)

### Run Locally

```bash
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) and start playing!

### Build for Production

```bash
npm run build
```

The built app auto-deploys to **GitHub Pages** when you push to `main`.

---

## 🎨 Customize Your Game

Make it yours! Adapt the questions to fit your event:

1. **Edit Questions** — Modify `src/data/questions.ts` with your own prompts
2. **Change the Theme** — Update colors and styles in `src/index.css`
3. **Tweak Game Logic** — Adjust win conditions in `src/utils/bingoLogic.ts`

**Pro tip:** Use the [Lab Guide](.lab/GUIDE.md) to explore AI-assisted customization with VS Code Copilot.

---

## 🧪 Tech Stack

- **React 19** with TypeScript for type-safe components
- **Vite 7** for lightning-fast builds
- **Tailwind CSS v4** for modern, maintainable styling
- **Vitest** for comprehensive testing
- **GitHub Pages** for seamless deployment

---

## 🤝 Contributing

This project is part of the [VS Code Agent Lab](https://github.com/microsoft/vscode-agent-lab-soc-ops) workshop. Whether you're learning about AI-assisted development or just want to make a cool bingo game — contributions are welcome!

Check out [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📝 License

MIT © [Harald Kirschner](https://github.com/digitarald)

---

**Ready to break the ice?** 🧊 [Play the demo](https://louloucodes.github.io/my-bingo-lab/) or fork this repo and make it your own!
