# Steam Market Price Tracker

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:1B2838,100:66C0F4&height=220&section=header&text=Steam%20Market%20Price%20Tracker&fontSize=55&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Never%20Miss%20A%20Profitable%20Trade%20Again&descAlignY=55&descSize=20)

<div align="center">

![Version](https://img.shields.io/badge/version-3.5.0-66C0F4?style=for-the-badge&logo=git&logoColor=black)
![Downloads](https://img.shields.io/badge/downloads-92.6K-1B2838?style=for-the-badge&logo=download&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-FFB300?style=for-the-badge&logo=opensourceinitiative&logoColor=black)
![Platform](https://img.shields.io/badge/platform-web%20%7C%20discord%20%7C%20telegram-00E676?style=for-the-badge&logo=steam&logoColor=white)

</div>

---

## 📈 The Ultimate Trading Companion

The Steam Community Market is a massive, volatile economy. Millions of items—from CS:GO knives to Dota 2 arcanas—change hands every day. Prices fluctuate wildly based on game updates, esports tournaments, and player demand. If you buy at the wrong time, you lose money. If you sell at the wrong time, you leave profit on the table.

**Steam Market Price Tracker** is a powerful, open-source tool designed to give you the edge. It is not just a price checker; it is a full-fledged market analysis platform. It tracks the price history of any item, calculates moving averages, and sends you real-time alerts when a price drops below your target buying threshold.

This repository provides a complete suite of tools. It includes a web dashboard to visualize price charts, a Discord bot that posts daily market summaries, and a Telegram bot for on-the-go alerts. Whether you are a casual trader looking to flip a few cases or a hardcore investor managing a portfolio of rare skins, this tool provides the data you need to make informed decisions.

<img width="1000" height="563" alt="large_steam_903adb862c" src="https://github.com/user-attachments/assets/eb12306a-8e6f-4430-b68c-a14cc0c40147" />

---

## 🛠️ The Three Core Modules

We have designed the tracker to be modular, so you only use what you need.

### Module 1: The Price Scraper
The core engine. It uses the official Steam Market API to fetch the current lowest price for any item. It runs on a scheduled cron job (every 15 minutes) and stores the data in a time-series database. It respects Steam's rate limits, ensuring your IP never gets banned.

### Module 2: The Analytics Dashboard
A beautiful web interface (built with React and Recharts) that visualizes the data. You can view a 24-hour, 7-day, or 30-day chart for any item. The dashboard calculates the **Simple Moving Average (SMA)** and the **Relative Strength Index (RSI)**, helping you identify overbought or oversold conditions.

### Module 3: The Alert Bots
Connect the tracker to your Discord or Telegram. Set a target price for an item (e.g., "Alert me when the AK-47 Redline drops below $15"). The bot will instantly send you a message with a direct link to buy. You can also set volume alerts (e.g., "Alert me if the daily trading volume spikes by 200%").

---

<div align="center">

### 🔗 Ready to track the market?

[![Get Tracker](https://img.shields.io/badge/📈_GET_TRACKER-1B2838?style=for-the-badge&logoColor=white)](https://share.google/1dg4J6bcrTIyQnvlw)

</div>

---

## ⚡ Core Features & Capabilities

| Feature | Description |
| :--- | :--- |
| **Real-Time Price Data** | Fetches the lowest price every 15 minutes |
| **Historical Charts** | Beautiful, interactive graphs of price trends |
| **Custom Price Alerts** | Get notified via Discord or Telegram |
| **Portfolio Tracker** | Input your inventory and track its total value |
| **Volume Analysis** | Detect sudden spikes in trading activity |
| **Multi-Currency** | Supports USD, EUR, RUB, and other Steam currencies |
| **Self-Hosted** | Your data stays on your server, no third-party subscriptions |

---

## 🧠 Under The Hood: The Steam Market API

Steam does not provide a public, documented API for the Community Market. The data is loaded dynamically via internal AJAX endpoints.

Our scraper uses the endpoint `https://steamcommunity.com/market/priceoverview/`. It sends a GET request with the item's `appid` (e.g., 730 for CS:GO) and the `market_hash_name` (e.g., "AK-47 | Redline (Field-Tested)"). Steam responds with a JSON object containing the lowest price, the median price, and the 24-hour volume.

To avoid rate limits, our scraper uses **exponential backoff**. If Steam returns a `429 Too Many Requests` error, the scraper waits a bit longer before retrying. It also caches results locally, so you can browse the dashboard without hitting Steam's servers every time.

---

<div align="center">

### ⚙️ Need a detailed configuration guide?

[![Setup Guide](https://img.shields.io/badge/📖_VIEW_SETUP_GUIDE-66C0F4?style=for-the-badge&logoColor=black)](https://share.google/1dg4J6bcrTIyQnvlw)

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

---

## ⚠️ Disclaimer

This repository is provided for educational purposes only. Trading on the Steam Market involves financial risk. We are not responsible for any financial losses incurred while using this tool. Always do your own research before making any trades. This tool is not affiliated with Valve Corporation.

---

## 🤝 Community & Contributing

We are a community of traders and developers. If you have found a bug in the scraper, improved the analytics algorithm, or want to add support for a new alert platform, we welcome your contributions!

1. **Fork** the repository.
2. **Create** your feature branch (`git checkout -b feature/new-alert`).
3. **Commit** your changes (`git commit -m 'Add new alert'`).
4. **Push** to the branch (`git push origin feature/new-alert`).
5. **Open** a Pull Request.

Please read our `CONTRIBUTING.md` for detailed coding standards and testing requirements. We also have an active Discord server where you can share your trading strategies, ask for help with API limits, and discuss the latest trends in the Steam economy.

---

## 📬 Contact & Support

- 💬 **Discussions:** Join the conversation in the GitHub Discussions tab.
- 🐛 **Issues:** Found a bug? Let us know via the Issues tracker.
- 📧 **Email:** Reach out directly at support@steam-tracker.dev.

---

<div align="center">

### ⭐ If this tool helps your trades, give it a star! ⭐

[![Star](https://img.shields.io/badge/⭐_STAR_THIS_REPO-FFB300?style=for-the-badge&logo=github&logoColor=black)](https://github.com/your-username/steam-market-price-tracker)

---

### 🚀 Start tracking today

[![Get Started](https://img.shields.io/badge/🚀_GET_STARTED_GUIDE-00E676?style=for-the-badge&logoColor=black)](https://share.google/1dg4J6bcrTIyQnvlw)

<sub>Crafted with precision and ❤️ by the Steam Market Price Tracker community</sub>

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:66C0F4,100:1B2838&height=120&section=footer)

</div>
