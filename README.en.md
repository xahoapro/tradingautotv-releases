[🇻🇳 Tiếng Việt](README.md) · **🇬🇧 English**

# TradingAutoTV — read signals on your TradingView chart, trade on MT5 / Binance Futures

**TradingAutoTV** is a Windows app that reads **the TradingView chart you have open** (strategy orders, shapes, indicator labels…) and places orders on **MetaTrader 5** or **Binance USDⓈ-M Futures** following the rules you set. No alerts, no webhooks.

### 👉 [Download the latest version](https://github.com/xahoapro/tradingautotv-releases/releases/latest) · [Tool introduction](https://tradingauto.org/toolintroduce/tradingview) · [Register](https://tradingauto.org/register) · [Buy a key](https://tradingauto.org/Pricing#tvbot)

---

## ✨ Features

**📈 Signals straight from the chart**
- Attaches to your open TradingView Desktop (or Chrome / Edge) and reads layouts, charts and indicators — read only, your chart is never changed.
- Triggers: strategy orders, shapes, text labels, lines, zones… The app proposes them by name (Long → open BUY, Short Exit → close SELL).
- ANY / ALL / AT LEAST k conditions within some bars, plus filters from other indicators.

**🤖 5-step bot wizard**
- Source → Conditions → Order rules → Capital → Review.
- SL / TP preset or taken from chart objects; several TP levels closed by %; trailing; break-even after TP1; skip when price has run too far.
- Fixed lot or risk based (USD / % equity), lot cap, stop when the loss / profit reaches a % of equity.
- **Magic number and comment per bot** to filter and group orders in MT5.

**🛡️ Safety first**
- A new bot always starts in **WATCH ONLY**: it reads the chart and MT5 checks the order without sending it — check the log, then switch to **TRADING**.
- Layout changed, chart minimized, account disconnected… the bot **pauses new orders** but can still close / modify existing ones, and resumes by itself when things are right again.
- REAL accounts require typing the account number again; the top bar turns red while a bot trades a real account.
- Bots that were running when the app closed restart when it opens again (per-bot switch).

**🏦 Many accounts**
- Each MT5 account gets a **clean** terminal cloned by the app (nobody's EAs, no saved passwords), running hidden, with an executor EA for fast bulk closing.
- Broker not on this computer yet: the app shows MT5 so you log in by hand **once**; later accounts reuse it.
- **Binance USDⓈ-M Futures** (new): testnet or live, SL / TP placed on the exchange. API keys with withdrawal permission are refused.
- Passwords / API keys only travel over 127.0.0.1 and are encrypted with Windows (DPAPI).

**📋 Log & overview**
- One overview for all bots, accounts and things that need attention; a full log of every signal and order.
- Vietnamese / English interface; an **Other products** page with the other TradingAuto tools.

## 🔑 License key

- Trading needs a **TradingAuto TradingView Bot license key**. One key is assigned to one account and runs in one place (this app, an EA or MT5 Manager).
- **Buy a key:** open [Pricing](https://tradingauto.org/Pricing#tvbot) → choose **📡 TradingView Bot** → follow the steps on the site (a tradingauto.org account is needed — [register](https://tradingauto.org/register) first if you have none). The **Buy a key** button in the app opens this page.
- **Demo accounts** and accounts opened under the **TradingAuto IB** use the built-in member key `vipmember` — **free**.
- Without a key you can still add accounts, create bots and run WATCH ONLY — you just cannot send new orders.

## 🚀 Getting started

1. **[Download the installer](https://github.com/xahoapro/tradingautotv-releases/releases/latest)**: `TradingAutoTV-<version>-setup.exe`, run it (no admin rights needed; installs to `%LOCALAPPDATA%\Programs\TradingAutoTV` with a Start Menu shortcut). If Windows shows "Windows protected your PC", click **More info → Run anyway**.
2. Start TradingView Desktop with `--remote-debugging-port=9222` (or Chrome / Edge with a separate profile on port 9223) and sign in to TradingView.
3. In the app: **License keys** → **MT5 accounts** (or Binance) → **＋ Bot from this layout** → run WATCH ONLY → check the log → **Switch to TRADING**.

The **Guide** section in the app walks through every step.

## 💻 Requirements

- Windows 10 / 11, 64-bit.
- MetaTrader 5 installed (the app clones terminals from your installation) — or a Binance Futures account.
- TradingView Desktop or Chrome / Edge. Keep each layout a bot uses in its own window, not minimized (TradingView stops updating minimized charts).
- The computer must stay on and online for bots to run (use a Windows VPS for 24/7).

## 🔄 Updates

The app tells you when a new version is out; one click downloads and installs it. If the new version fails to start, the app returns to the previous one; your data (`data\`) is kept. Update packages are **signed** — the app only accepts official builds.
The `-update.zip` and `latest.json` files under Releases are for the self-updater — new users should download the **`-setup.exe`** file.

## 💬 Support & community

- Website: **[tradingauto.org](https://tradingauto.org)**
- Zalo group: [zalo.me/g/scuqhg283](https://zalo.me/g/scuqhg283) · Telegram group: [t.me/autotradingfreeall](https://t.me/autotradingfreeall)
- Other tools: [MT5 Manager](https://github.com/xahoapro/mt5manager-releases) · [Copytrade Online](https://tradingauto.org/toolintroduce/copytrade) · [Smart DCA](https://tradingauto.org/toolintroduce/dcabot) · [Copy Signal → MT5](https://tradingauto.org/toolintroduce/signaltrader)

> ⚠️ TradingAutoTV executes the rules you set — it **does not predict the market and does not guarantee profit**. Trading forex / CFDs / crypto futures carries high risk. Run WATCH ONLY and a demo account first.
