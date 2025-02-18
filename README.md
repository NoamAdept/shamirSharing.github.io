# shamirSharing.github.io
# Shamir Secret Sharing Web App

A Flask-based web application demonstrating **Shamir Secret Sharing**. The app lets you encode a message into a secret number, split it into shares using a random polynomial, and reconstruct the secret from a subset of those shares.

## Overview

For a secret \( m \) over \( \mathbb{Z}_p \), we generate a random polynomial:
\[
f(x) = m + a_1 x + a_2 x^2 + \dots + a_{t-1} x^{t-1} \pmod{p}
\]
- **Shares:** Each share is a point \( (i, f(i) \mod p) \).
- **Threshold:** At least \( t \) shares are required to reconstruct \( m = f(0) \) via Lagrange interpolation.

*Example:* Over \( \mathbb{Z}_{11} \) with \( m = 7 \) and \( t=3 \) (3-out-of-5):
\[
f(x) = 1\cdot x^2 + 4\cdot x + 7 \quad \Rightarrow \quad \{(1,1), (2,8), (3,6), (4,6), (5,8)\}
\]
Any 3 shares can recover \( m \).

## Features

- **Message Encoding/Decoding:** Convert text to a secret number and back.
- **Interactive UI:** Use sliders to set the secret, total shares \( n \), and threshold \( t \).
- **Share Generation & Download:** Generate shares and download each as a text file.
- **Share Upload:** Upload share files to reconstruct the secret.
- **Visualization:** Plot share points (and optionally the polynomial curve) using Plotly.


