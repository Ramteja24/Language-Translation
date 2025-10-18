# 🌐 Language Translator

A simple yet powerful **Language Translation Web Application** built using **Vanilla JavaScript, HTML, and CSS**.  
It allows users to translate any text or phrase from one language to another seamlessly, using open-source or third-party translation APIs such as **Google Translate API**, **LibreTranslate**, or **DeepL API**.

This project emphasizes a **minimalistic UI**, **fast performance**, and **flexibility** to integrate with any translation backend you prefer.

---

## 🚀 Demo

<img width="1200" height="600" alt="Language Translator Preview" src="https://github.com/user-attachments/assets/9fd4b9d7-68e5-4162-9e52-5d29e88ea081" />

---

## ✨ Features

- 🌍 **Translate Text Instantly:** Supports multiple languages and auto-detection of source language.  
- 💻 **Clean, Responsive UI:** Simple and adaptable design that works across all devices.  
- ⚡ **Fast Fetch-Based Translation:** Uses JavaScript’s `fetch()` for smooth and fast API requests.  
- 📋 **Copy & Download Support:** Easily copy translated text or download it for later use.  
- 🔄 **Dynamic Language Selection:** Choose source and target languages from a large list (powered by `Countries.js`).  
- 🧠 **API-Agnostic Design:** Easily replace or switch between translation APIs (e.g., LibreTranslate, Google Translate, DeepL).  
- 🛠️ **Error Handling & Feedback:** Provides loading indicators and error messages for a seamless user experience.  
- 📱 **Lightweight & Browser-Friendly:** Works without heavy frameworks — just HTML, CSS, and JS!

---

## 🗂️ Project Structure

```bash
language-translator/
├── index.html        # Main HTML page (UI layout)
├── style.css         # CSS for styling and responsiveness
├── script.js         # Main JavaScript logic (API calls and DOM handling)
├── Countries.js      # Contains language codes and names for dropdowns
├── README.md         # Documentation file (you’re reading it!)


**🛠️ Prerequisites**

Modern browser (Chrome, Firefox, Edge)

Node.js (only if you run a local backend or proxy)

An API key for the translation service you choose (if using a hosted API)

If you want a free option for experimenting, consider:

LibreTranslate — public instances exist, or you can self-host: https://libretranslate.com

Or deploy a tiny backend proxy and store your API keys server-side.

**⚙️ Installation & Quick Start**
Option A — Frontend-only (using a public/free translation endpoint)

Clone the repo or copy the files to a folder.

Edit script.js to point to the translation API endpoint you’ll use (examples below).

Open index.html in your browser.

Option B — Frontend + Local proxy server (recommended for API keys)

Put your API key in a .env file (or server environment variable).

Run the small Node/Express proxy (example below).

Open index.html and the frontend will call your proxy at /api/translate.
<img width="1083" height="655" alt="image" src="https://github.com/user-attachments/assets/100df4c3-9530-4274-964e-767ba49ee3c7" />
