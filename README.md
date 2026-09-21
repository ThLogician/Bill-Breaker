# Bill Breaker

Drop in a medical bill or insurance EOB and get plain-English flags for common billing errors, plus a ready-to-send dispute letter and phone script.

## How to run

Open `index.html` in any modern browser. An internet connection is required on first load — the app fetches **pdf.js** from a CDN to read PDF files.

## Try it in 3 steps

1. Click **ER visit**, **Lab work**, or **Insurance denial** to load a built-in sample, or drop `sample-medical-bill.pdf` / `sample-denial-eob.pdf` onto the text area.
2. Tick **In-network provider** if that applies, then click **Find errors**.
3. Review the flagged cards, then scroll down to copy or print your personalised **Dispute letter** or **Phone script**.

## Detection rules

| Rule | What it catches |
|---|---|
| **Duplicate charge** | Same CPT code billed more than once on the same date for the same amount |
| **Unbundled charges** | A component code billed alongside its parent code (e.g. 80048 + 80053, 85027 + 85025) |
| **Multiple E/M same day** | More than one evaluation & management visit (99211–99215) charged on the same date |
| **Repeated venipuncture** | Code 36415 billed more than once on the same day |
| **Missing in-network adjustment** | In-network provider with no contractual discount applied to a line ≥ $100 |
| **Denial codes** | Recognised CARC/RARC codes in the text: CO-16, CO-50, CO-97, CO-197, PR-1 |

## Privacy

All processing happens entirely in your browser. No bill text, PDF content, or personal information is ever sent to a server or leaves your computer.

## What's next

- More unbundling pairs and denial codes
- Side-by-side EOB vs. bill comparison
- Export findings to CSV
