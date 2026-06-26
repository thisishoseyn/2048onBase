# 🎮 Base On-Chain 2048 Arena

A modern, high-contrast, fully client-side **2048 game** integrated with the **Base L2 blockchain** for verifiable global high scores. 

🚀 **Live Demo:** [2048onbase-eosin.vercel.app](https://2048onbase-eosin.vercel.app/)

---

## 🛡️ Security & Architecture

This project is built from scratch with a **security-first** approach for the Web3 ecosystem:
- **Zero Approvals Required:** The integration only invokes a simple execution method (`submitScore`). It **never** requests any token approvals, wallet control, or asset interaction. Your digital assets remain entirely isolated and safe.
- **Pure Client-Side:** No centralized backend servers, tracking scripts, or database dependencies. Everything runs directly inside your browser.
- **Lightweight Web3 Integration:** Uses `ethers.js` via secure CDN to interact directly with the Base RPC network and MetaMask/Web3 wallets.

---

✨ Features:

Fluid 2048 Gameplay: Smooth transitions, immediate keyboard arrow tracking (W, A, S, D), and full mobile responsive touch/swipe gestures.

Immediate Color Burst: The vibrant visual themes initiate immediately from tile 4 onwards for an immersive arcade feel.

On-Chain Leaderboard: Fetches and filters real-time transaction logs from the Base network to display a decentralized top-5 player ranking.

Glassmorphic UI / Theme Toggle: Supports a beautiful dynamic shift between Neo-Dark and High-Contrast Light Mode with persistent layer blur effects.

---

🛠️ Local Development
Since this project has no external Node.js dependencies, you can run it locally in seconds:

1. Clone the repository:
   git clone https://github.com/thisishoseyn/2048onBase.git

2. Open 2048.html directly in any modern browser.

---

📄 License
This project is open-source and available under the MIT License. Made with ❤️ by Hoseyn.

---

## 📜 Smart Contract Details

The game interacts with a verified high-score contract deployed on the **Base Mainnet**:

- **Contract Address:** `0xBB26CDfa52BE78aCeA953786ad925bd61b24A8F0`
- **Network:** Base Mainnet (Chain ID: `8453`)

### Contract ABI Used:
```javascript
[
    "function submitScore(uint256 _score) external",
    "function getTotalGames() external view returns (uint256)",
    "function topGames(uint256) external view returns (address playerAddress, uint256 highScore, uint256 timestamp)",
    "event NewHighScore(address indexed player, uint256 score, uint256 timestamp)"
]

