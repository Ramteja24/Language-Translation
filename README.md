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


⚙️ Installation & Quick Start
🅰️ Option A — Frontend Only (Free / Public API)

If you just want to test the app with a public translation endpoint:

Clone or download this repository:

git clone https://github.com/your-username/language-translator.git


Open the project folder:

cd language-translator


Open index.html in your web browser.

Enter your text → choose languages → click Translate 🚀

🅱️ Option B — Frontend + Local Proxy Server (Recommended for API keys)

To securely use APIs that require authentication (like Google or DeepL):

Create a .env file and add your API key:

TRANSLATE_API_KEY=your_api_key_here


Create a lightweight Node.js Express proxy (server.js):

import express from "express";
import fetch from "node-fetch";
import dotenv from "dotenv";
dotenv.config();

const app = express();
app.use(express.json());

app.post("/api/translate", async (req, res) => {
  const { text, source = "auto", target = "en" } = req.body;
  try {
    const response = await fetch("https://api.example.com/translate", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": `Bearer ${process.env.TRANSLATE_API_KEY}`
      },
      body: JSON.stringify({ q: text, source, target })
    });

    const data = await response.json();
    res.json({ translatedText: data.translatedText });
  } catch (error) {
    console.error(error);
    res.status(500).json({ error: "Translation failed" });
  }
});

app.listen(3000, () => console.log("✅ Server running at http://localhost:3000"));


Run the proxy:

npm install express node-fetch dotenv
node server.js


Open index.html — it will now call your proxy endpoint (/api/translate) securely.
