# Shamir Secret Sharing Web App 🔐✨

Welcome to the **Shamir Secret Sharing Web App** – a fun, interactive Flask-based tool that demonstrates the magic of Shamir Secret Sharing! This app lets you convert a message into a secret number, split it into multiple shares using a random polynomial, and reconstruct the secret when enough shares come together. Let’s dive in! 🚀

---

## Overview 🧐

Imagine you have a secret \( m \) over \( \mathbb{Z}_p \). With our app, we generate a random polynomial:
$\[
f(x) = m + a_1 x + a_2 x^2 + \dots + a_{t-1} x^{t-1} \pmod{p}
\]$
- **Shares:** Each share is represented as a point \( (i, f(i) \mod p) \).
- **Threshold:** At least \( t \) shares are needed to reconstruct the secret \( m = f(0) \) via Lagrange interpolation.

### Example 📊
Consider a scenario over \( \mathbb{Z}_{11} \) with:
- Secret \( m = 7 \)
- Threshold \( t = 3 \) (3-out-of-5 scheme)

The polynomial might look like:
\[
f(x) = 1\cdot x^2 + 4\cdot x + 7
\]
Which generates the shares:
\[
\{(1,1),\; (2,8),\; (3,6),\; (4,6),\; (5,8)\}
\]
With any **3 shares**, you can recover the secret \( m \)! 🔍

---

## Features 🎉

- **Message Encoding/Decoding:**  
  Convert your text messages to a secret number and back – making cryptography accessible and fun! ✉️🔄

- **Interactive UI:**  
  Use intuitive sliders to set your secret, total shares \( n \), and threshold \( t \). Adjust parameters on the fly and see the magic happen! 🎛️🖱️

- **Share Generation & Download:**  
  Easily generate shares and download each one as a text file. Perfect for secure storage and sharing! 💾📤

- **Share Upload:**  
  Reconstruct your secret effortlessly by uploading the share files. Collaboration and security go hand in hand! 🤝🔓

- **Visualization:**  
  Enjoy dynamic plots of your share points (and optionally the polynomial curve) using Plotly. Visualize your secret’s journey from creation to reconstruction! 📈🎨

---

Get ready to explore the fascinating world of cryptography with our Shamir Secret Sharing Web App. Secure your secrets and share with confidence! 🔑🌟

Happy sharing! 😄

---

*This project is open-source and designed to educate and empower. Dive into the code and contribute to making secure sharing accessible to everyone!* 💻❤️
