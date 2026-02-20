# 🧾 GSTR-2A Reconciliation Tool
### Created by **Harsh Mevada** · CA Tools India

> Upload your GSTR-2A and Tally Purchase Register → Get a fully reconciled Excel in seconds.
> **₹5 per reconciliation · 100% refund if it doesn't work**

---

## 📌 What Is This?

Every month, GST-registered businesses must check whether the **Input Tax Credit (ITC)** shown in their **GSTR-2A** (auto-populated from suppliers on the GST portal) matches their **Tally Books (Purchase Register)**.

This is called **GSTR-2A Reconciliation** — and doing it manually in Excel can take **2–4 hours**.

This tool does it in **under 30 seconds**.

---

## ✅ How To Use (Non-Technical Guide)

### Step 1 — Pay ₹5

- Open the tool link in your browser
- Scan the **QR code** on screen with GPay / PhonePe / Paytm / BHIM
- Pay ₹5 and note the **UTR / Transaction ID** shown in the payment confirmation
- Enter the UTR in the unlock box and click **"Unlock Tool"**

> 💚 **100% Refund Guarantee** — If the tool doesn't work for your file, share a screenshot and get a full refund. No questions asked.

---

### Step 2 — Get Your Files Ready

| File | Where to download |
|------|------------------|
| **GSTR-2A** | GST Portal → Login → Return Dashboard → GSTR-2A → Download Excel |
| **Purchase Register** | Tally → Gateway of Tally → Display → Account Books → Purchase Register → Export to Excel |

Both `.xls` and `.xlsx` formats are supported.

---

### Step 3 — Upload & Run

1. Upload **GSTR-2A file** in the left box
2. Upload **Purchase Register** in the right box
3. Click ⚡ **Run Reconciliation**
4. Wait ~15 seconds
5. Click 📥 **Download Reconciliation Excel**

---

## 📊 What's Inside the Output Excel?

You get a colour-coded Excel file with **5 sheets**:

| Sheet | Colour | What It Means |
|-------|--------|---------------|
| 📊 Summary | — | Overall counts + GST amount comparison (2A vs Books) |
| ✅ Matched Exact | 🟢 Green | Perfect match — same vendor, same GST amount |
| ✅ Matched (±₹10) | 🟡 Yellow | GST differs by ≤₹10 — treated as matched (rounding differences) |
| ⚠️ Unmatched in 2A | 🔴 Red | In GSTR-2A but **missing in your Books** — **ITC risk! Investigate these** |
| ⚠️ Unmatched in Books | 🔴 Red | In your Books but **missing from 2A** — supplier may not have filed their GST return |

---

## 🧠 How The Matching Works

**Vendor Name — Fuzzy Matching:**
The tool uses intelligent fuzzy matching so minor typos between Tally and the GST portal are handled automatically. For example:
- `H A Construction` ↔ `H.A.CONSTRUCTION` ✅ Matched
- `COCOBUL RETAIL LIMITED` ↔ `COCOBLU RETAIL LIMITED` ✅ Matched
- `BRAINSTROM INFOTECH` ↔ `BRAINSTORM INFOTECH` ✅ Matched

**GST Amounts — ±₹10 Tolerance:**
If CGST, SGST, or IGST differ by ₹10 or less (due to rounding), the record is still treated as **matched** and shown in yellow.

**No GSTIN Matching:**
The tool matches by vendor name + GST amount — not GSTIN — to handle data entry differences between Tally and the portal.

---

## 🔒 Data Security

- ✅ Your files are **never saved or stored** anywhere
- ✅ Everything runs in temporary memory — like a calculator
- ✅ When you close the browser, all data is permanently gone
- ✅ Your files are **never visible to anyone else**, including the developer
- ✅ Each session is 100% isolated and private

---

## ❓ FAQ

**Q: Do I need to install anything?**
No. Open the link in any browser — Chrome, Firefox, Safari, Edge. Works on phone and desktop.

**Q: What if my file format is different?**
The tool is built for the standard GSTR-2A export from the GST portal and Tally's Purchase Register export. If your columns are different, contact for support.

**Q: Can two people use it at the same time?**
Yes. Every session is completely separate.

**Q: What if I paid but the tool shows an error?**
WhatsApp a screenshot to get a full refund. The tool also shows detailed error messages to help diagnose the issue.

**Q: Is the ₹5 per use or per month?**
Per reconciliation. Each time you run a new report, pay ₹5 and enter the new UTR.

**Q: Will it work for any financial year?**
Yes — the tool works for any period as long as the file format matches.

---

## 🛠️ For Developers

### Tech Stack
- **App:** Python + Streamlit
- **Excel I/O:** openpyxl + xlrd
- **Matching:** difflib SequenceMatcher (fuzzy)
- **Hosting:** Streamlit Community Cloud (free)
- **Payment:** UPI QR code (honour-based UTR verification)

### Files
```
gstr-reco-pro/
├── app.py            ← Main Streamlit app
├── requirements.txt  ← Python dependencies
└── README.md         ← This file
```

### Deploy on Streamlit Cloud (Free)

1. Create a GitHub account at [github.com](https://github.com)
2. Create a new repository named `gstr-reco-pro`
3. Upload `app.py`, `requirements.txt`, `README.md`
4. Go to [share.streamlit.io](https://share.streamlit.io)
5. Sign in with GitHub → Create app → select repo → Main file: `app.py` → Deploy

Your app goes live in ~3 minutes at a URL like:
`https://harshmevada-gstr-reco-pro.streamlit.app`

### Update the App
Edit `app.py` directly on GitHub → Streamlit auto-redeploys in ~1 minute.

---

## 📞 Contact & Support

**Created by Harsh Mevada**

For support, refund requests, or custom requirements — reach out directly.

> 💚 If the tool saves you time, share it with your CA friends!

---

*GSTR-2A Reconciliation Tool · FY 2025-26 · Made in India 🇮🇳*
*Fuzzy name matching · ±₹10 tolerance · Zero data storage · ₹5 per use*
