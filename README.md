# 📊 Distribution Probability Tool  
### Canvas-Embeddable Probability Calculator (Binomial • Poisson • Normal)

A single-file, client-side HTML tool for computing probabilities from:

- **Binomial** (exact or Normal approximation with continuity correction)
- **Poisson** (exact or Normal approximation with continuity correction)
- **Normal** (exact; μ and σ may be entered or estimated from pasted data)

Designed specifically to be hosted on **GitHub Pages** and embedded in **Canvas** via `<iframe>`.

---

## ✨ Features

### ✅ Probability Forms Supported
- P(X ≤ x)
- P(X ≥ x)
- P(X < x)
- P(X > x)
- P(X = x)
- P(a ? X ? b)


---

### 📌 Distribution Capabilities

#### **Binomial**
- Exact PMF & CDF
- Optional **Normal approximation**
- Automatic continuity correction
- Integer interpretation for counts

#### **Poisson**
- Exact PMF & CDF
- Optional **Normal approximation**
- Automatic continuity correction
- Integer interpretation for counts

#### **Normal**
- Exact probability via CDF
- Optional estimation of μ and σ from pasted data
- Correct handling of:
  - \( P(X = x) = 0 \)
  - \( P(X ≤ x) = P(X < x) \)

---

### Normal Approximation (Discrete)

Continuity correction rules used internally:

| Query | Approximation Used |
|-------|-------------------|
| P(X ≤ x) | P(Y ≤ x + 0.5) |
| P(X < x) | P(Y ≤ x − 0.5) |
| P(X ≥ x) | P(Y ≥ x − 0.5) |
| P(X > x) | P(Y ≥ x + 0.5) |
| P(X = x) | P(x − 0.5 < Y < x + 0.5) 
---

## 🚀 Deployment on GitHub Pages

1. Upload `probability_tool.html` to your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**:
   - Source: `Deploy from a branch`
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
4. Save.

Your tool will publish at:
https://YOUR-USERNAME.github.io/YOUR-REPO/probability_tool.html



## 🎓 Embed in Canvas

Edit a Canvas page → Switch to **HTML editor** → Paste:

```html
<iframe
  src="https://YOUR-USERNAME.github.io/YOUR-REPO/probability_tool.html"
  width="100%"
  height="900"
  style="border:0;">
</iframe>

> ⚠️ Important: Use the `github.io` URL — not `github.com`.  
> Canvas blocks embedded `github.com` pages.
```
---

## 📜 License

This project is licensed under the **MIT License**.

You are free to:

- Use  
- Modify  
- Distribute  
- Embed in LMS platforms (including Canvas)  
- Adapt for instructional or institutional use  

As long as the original license notice is included.

See the `LICENSE` file in this repository for the full text of the MIT License.

---

## 🎓 Intended Use

This tool was developed for instructional use in:

- Introductory Statistics  
- Probability  
- Business Statistics  
- Engineering Statistics  

It is:

- Fully client-side (no server required)  
- No data storage  
- No tracking  
- No external dependencies  

Designed specifically for easy deployment via **GitHub Pages** and embedding into learning management systems such as **Canvas**.

---

