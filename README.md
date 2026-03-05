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


----

## **Updated Functionality** 
🔁 Inverse Normal (Find x from a Probability)

This tool now includes **Inverse Normal** functionality.

Use the **Mode** dropdown in the Probability Query panel:

- **Probability (find P)** → computes a probability from x (or between a and b)
- **Inverse (Normal only — find x)** → computes x (or bounds) from a probability p

> Inverse mode is available for **Normal(μ, σ)** only.

### Inverse Options

In **Inverse** mode, choose one of the following:

1) **Find x such that P(X ≤ x) = p**  
   - Input: p  
   - Output: x (the p-th percentile of Normal(μ, σ))

2) **Find x such that P(X ≥ x) = p**  
   - Input: p  
   - Output: x (right-tail cutoff)  
   - Internally uses: P(X ≤ x) = 1 − p

3) **Find bounds a, b such that P(a ≤ X ≤ b) = p (centered about μ)**  
   - Input: p  
   - Output: symmetric bounds a and b around μ  
   - Returns: a = μ − zσ and b = μ + zσ

### Notes
- p must satisfy: **0 < p < 1**
- Normal is continuous, so **P(X = x) = 0** and **≤ vs < gives the same result**.

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

## 📱 Install as a Mobile App (PWA)

This calculator can be installed on a phone or tablet and used like a normal app.

### Android (Chrome)

1. Open the app in Chrome:

   https://mathwiz961.github.io/ProbabilityCalculator/

2. Tap the **⋮ menu** in the upper right.
3. Select **Install App** or **Add to Home Screen**.
4. Confirm installation.

The **Probability Calculator** will appear with your other apps and can run offline.

---

### iPhone / iPad (Safari)

1. Open the app in **Safari**:

   https://mathwiz961.github.io/ProbabilityCalculator/

2. Tap the **Share** button.
3. Scroll down and choose **Add to Home Screen**.
4. Tap **Add**.

The app icon will appear on your home screen.

---

## 🌐 Embedding in Canvas or Other LMS

The calculator can be embedded using an iframe:

```html
<iframe
src="https://mathwiz961.github.io/ProbabilityCalculator/"
width="100%"
height="900"
style="border:0;">
</iframe>

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

