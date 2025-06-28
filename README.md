sheeshcoin-site/
├── public/
│   └── index.html
├── src/
│   ├── main.jsx
│   ├── SheeshLanding.jsx
│   └── index.css
├── package.json
├── vite.config.js
└── README.md
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>SheeshCoin</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import SheeshLanding from './SheeshLanding';

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <SheeshLanding />
  </React.StrictMode>
);
import { useState } from 'react';

export default function SheeshLanding() {
  const [tokenomics] = useState({ supply: '1 Trillion', liquidityFee: '1%', marketingFee: '1%' });

  return (
    <main style={{ background: 'linear-gradient(to bottom, #7e22ce, #ec4899)', color: 'white', padding: '2rem' }}>
      <section style={{ textAlign: 'center', padding: '3rem 0' }}>
        <h1 style={{ fontSize: '4rem', fontWeight: 'bold' }}>🔥 SheeshCoin</h1>
        <p style={{ fontSize: '1.25rem' }}>The viral meme coin taking over Base Chain</p>
        <p style={{ fontSize: '0.875rem', marginTop: '0.5rem' }}>Built for memes. Fueled by hype. Locked by UniCrypt.</p>
        <div style={{ marginTop: '1.5rem' }}>
          <a href="#" style={{ fontSize: '1.125rem', padding: '0.75rem 1.5rem', backgroundColor: '#facc15', color: 'black', textDecoration: 'none', borderRadius: '8px' }}>
            Buy on Uniswap
          </a>
        </div>
      </section>

      <section style={{ display: 'grid', gap: '1.5rem', gridTemplateColumns: 'repeat(auto-fit, minmax(200px, 1fr))', padding: '2rem 0' }}>
        <div style={{ backgroundColor: '#ec4899', padding: '1.5rem', borderRadius: '12px' }}>
          <h2 style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>💰 Total Supply</h2>
          <p>{tokenomics.supply}</p>
        </div>
        <div style={{ backgroundColor: '#9333ea', padding: '1.5rem', borderRadius: '12px' }}>
          <h2 style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>💧 Liquidity Fee</h2>
          <p>{tokenomics.liquidityFee}</p>
        </div>
        <div style={{ backgroundColor: '#2563eb', padding: '1.5rem', borderRadius: '12px' }}>
          <h2 style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>📣 Marketing Fee</h2>
          <p>{tokenomics.marketingFee}</p>
        </div>
      </section>

      <section style={{ textAlign: 'center', padding: '2rem 0' }}>
        <h2 style={{ fontSize: '2rem', fontWeight: 'bold' }}>🔒 Liquidity Locked on UniCrypt</h2>
        <p>SheeshCoin is 100% rug-proof with liquidity locked for 12 months.</p>
        <a href="https://app.unicrypt.network" target="_blank" rel="noreferrer" style={{ marginTop: '1rem', display: 'inline-block', padding: '0.75rem 1.5rem', backgroundColor: 'white', color: '#7e22ce', textDecoration: 'none', borderRadius: '8px' }}>
          View Lock on UniCrypt
        </a>
      </section>

      <section style={{ textAlign: 'center', padding: '2rem 0' }}>
        <h2 style={{ fontSize: '1.875rem', fontWeight: 'bold' }}>📜 Read the Whitepaper</h2>
        <p>Understand the mission, tokenomics, and roadmap for SheeshCoin.</p>
        <a href="/SheeshCoin_Whitepaper.pdf" target="_blank" rel="noreferrer" style={{ marginTop: '1rem', display: 'inline-block', padding: '0.75rem 1.5rem', backgroundColor: '#facc15', color: 'black', textDecoration: 'none', borderRadius: '8px' }}>
          Download PDF
        </a>
      </section>

      <footer style={{ textAlign: 'center', marginTop: '2rem', fontSize: '0.875rem', color: 'rgba(255, 255, 255, 0.7)' }}>
        © 2025 SheeshCoin. All memes reserved.
      </footer>
    </main>
  );
}
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
{
  "name": "sheeshcoin-site",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "vite": "^4.0.0",
    "@vitejs/plugin-react": "^3.0.0"
  }
}
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()]
});
# SheeshCoin Site

This is the React + Vite landing page for SheeshCoin — a viral meme coin on Base with auto-liquidity and UniCrypt lock.

## How to run locally

```bash
npm install
npm run dev
