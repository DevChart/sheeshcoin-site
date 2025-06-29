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
    "vite": "^4.3.9",
    "@vitejs/plugin-react": "^3.1.0"
  }
}
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()]
});
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
import SheeshLanding from './SheeshLanding';
import './index.css';

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <SheeshLanding />
  </React.StrictMode>
);
export default function SheeshLanding() {
  return (
    <main style={{ padding: '2rem', fontFamily: 'Arial, sans-serif', background: '#f7f0ff', minHeight: '100vh' }}>
      <h1 style={{ color: '#9333ea' }}>🔥 SheeshCoin</h1>
      <p>The viral meme coin on Base Chain</p>
      <a href="#" style={{ display: 'inline-block', marginTop: '1rem', padding: '0.75rem 1.5rem', backgroundColor: '#facc15', color: '#000', textDecoration: 'none', borderRadius: '8px' }}>
        Buy on Uniswap
      </a>
    </main>
  );
}
body {
  margin: 0;
  background-color: #f7f0ff;
  color: #444;
}
