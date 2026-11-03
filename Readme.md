# ETIT 🕵️‍♂️💬

<p align="center">
  <b>A sleek, client-side steganography web app for hiding secret messages inside normal cover text using zero-width characters.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success.svg" alt="Status Active">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/technology-HTML5%20%7C%20CSS3%20%7C%20JavaScript-orange.svg" alt="Tech Stack">
</p>

---

## 🚀 Overview

**ETIT** is a lightweight, modern web utility that allows you to embed confidential text messages directly inside ordinary, innocent-looking cover text. It achieves this by mapping binary data streams to **zero-width Unicode characters** (such as the Zero-Width Non-Joiner and Zero-Width Joiner) appended seamlessly into the text string. 

Because zero-width characters are invisible to the naked eye, the carrier text appears entirely normal when pasted into messaging apps, documents, or social media—while still carrying a hidden payload readable by anyone using the decoder.

---

## ✨ Features

* **Encode Mode:** Combine any normal "Cover Text" with a "Secret Text" to produce a disguised payload instantly.
* **Decode Mode:** Paste suspicious or encoded text to instantly extract and reveal the hidden message.
* **Signature Verification:** Utilizes a secure internal signature byte-sequence (`ETIT`) to ensure decoded payloads are valid and intended.
* **One-Click Actions:** Quick copy and clear buttons for efficient workflow.
* **Modern UI/UX:** Built with a clean, dark-mode glassmorphism aesthetic inspired by modern developer tools, featuring responsive grid layouts and smooth transitions.
* **100% Client-Side:** Runs completely in your browser with zero server requests or external tracking.

---

## 🛠️ How It Works (Under the Hood)

1. **Binary Conversion:** Secret text strings are converted into UTF-8 binary bytes using the browser's `TextEncoder`.
2. **Zero-Width Mapping:** 
   * `0` $\rightarrow$ Zero-Width Non-Joiner (`\u200C`)
   * `1` $\rightarrow$ Zero-Width Joiner (`\u200D`)
   * Bytes are separated by a Zero-Width Space (`\u200B`).
3. **Payload Assembly:** The application prefixes the hidden data with a custom byte signature (`ETIT`) followed by the encoded secret stream appended directly to the end of the cover text.

---

## 📦 Getting Started

Since ETIT is built purely using vanilla web technologies (HTML5, CSS3, and JavaScript), there are no build steps, package managers, or complex dependencies required to run it.

### Prerequisites
* Any modern web browser (Chrome, Firefox, Safari, Edge).

### Running Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/etit.git](https://github.com/your-username/etit.git)