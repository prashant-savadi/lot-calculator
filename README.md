# 📊 Lot Calculator

A fast, beautiful, single-file web tool to calculate how many lots you can buy with a given investment, total cost per lot size, and your exit price based on a configurable loss percentage.

---

## ✨ Features

- **Default Lot Sizes** — Toggle chips for 20, 25, 30, 50, 60, 65, 75; **20 and 65 are enabled by default**, others can be toggled on as needed
- **Custom Lots** — Add any lot sizes (single or comma-separated)
- **Loss Exit Price** — Defaults to 15%; set any % to instantly see at what price you should exit
- **Summary Panel** — Max qty, price/share, loss amount, exit price, total amount at a glance
- **Lot Breakdown Table** — Per lot: quantity (tap to copy), total cost, loss amount, and exit price (tap to copy)
- **Mobile & Desktop Friendly** — Fully responsive layout
- **No dependencies** — Single `index.html`, loads instantly with zero external JS

---

## 🚀 Usage

1. Open `index.html` in any modern browser — no server required.
2. Fill in:
   - **Amount (₹)** — Your total investable capital
   - **Current Price (₹)** — The stock/asset's current price
   - **Loss % (exit trigger)** — At what % loss should you exit? (default: 15)
   - **Custom Lots** _(optional)_ — Any additional lot sizes, comma-separated (e.g. `100, 200, 500`)
3. Toggle on/off lot sizes using the chips — **20** and **65** are on by default; 25, 30, 50, 60, 75 are available but off by default.
4. Hit **Calculate** (or press `Enter`).

---

## 🧮 How It Works

| Field                    | Formula                              |
| ------------------------ | ------------------------------------ |
| Qty (for lot N)          | `floor(Amount ÷ Price ÷ N) × N`      |
| Total Cost               | `Qty × Price`                        |
| Loss Amount _(per lot)_  | `Total Cost × (Loss% ÷ 100)`         |
| Exit Price               | `Price × (1 − Loss% ÷ 100)`          |
| Loss Amount _(summary)_  | `Amount × (Loss% ÷ 100)`             |

---

## 📁 Project Structure

```text
lot-calculator/
├── index.html   # The entire app — single file
├── README.md    # This file
└── LICENSE      # Individual developer use only
```

---

## ⚖️ License

This project is licensed under the **Individual Developer License**.  
See [LICENSE](./LICENSE) for full terms.

> ⚠️ **Not permitted** for commercial products, SaaS platforms, or team/enterprise use without explicit written permission from the author.

---

## 👤 Author

**Prashant Savadi**  
📧 [prsh.jkd@gmail.com](mailto:prsh.jkd@gmail.com)  
🔗 [linkedin.com/in/prashant-savadi](https://www.linkedin.com/in/prashant-savadi)

---

_© 2026 Prashant Savadi. All rights reserved._
