# BankStatementAnalysisTool

This is a small client-side tool that parses bank statement exports (HDFC netbanking Excel) and provides a categorized ledger and dashboard of spending and incoming transactions. It runs fully in the browser and does not transmit or store your data.

Main features
- Drop an HDFC statement (.xls/.xlsx) to get an instant spend breakdown by category, monthly trends, and a credits ledger.
- Automatic categorization rules for expenses and credits; rules are defined in `index.html` (editable lists of narration keywords).
- Investment and mutual fund transactions are separated from everyday spend.
- Collapsible category ledger (parent → child → subchild) so you can drill into Salary, Rent, Grocery (Milk Basket / Dmart / Other), Sports & fitness, Utility Bill Payments, and more.

Quick developer notes
- The main UI and logic live in `index.html` (single-file client app). Edit the keyword lists and category groupings there to tune classification.
- A `.gitignore` is included so only `.html` files are kept for commits by default. If you previously committed other files and want the .gitignore enforced, run:

  git rm -r --cached .
  git add .
  git commit -m "Apply .gitignore: keep only html in future commits"

- If you want to allow other files (CSS, JS, images) update `.gitignore` and un-comment or add allow rules.

Privacy & security
- The app runs entirely client-side using SheetJS and Chart.js loaded from CDNs. No uploaded files are transmitted.

Extending categories
- To improve classification add more narration fragments to the arrays in `index.html` (see `INCOME_RULES` and `EXPENSE_RULES`). If you want I can help tune these rules for your statements.

Contact / Contribution
- This is intended as a personal tool. Fork and adapt as needed; open a PR if you want me to review changes.

---
Generated .gitignore excludes all files except HTML and the README/.gitignore so that commits stay focused on UI changes.
