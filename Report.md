# TasteTreak – Project Report

---

## 1. 🧠 Project Overview

**TasteTreak** is a Telugu voice-enabled Streamlit web application designed to make food discovery both educational and enjoyable. It allows users to:
- Learn the **cultural and historical background** of traditional Telugu dishes.
- Get **recipe suggestions** based on spoken or typed **ingredients** — all in **Telugu**.

By combining **offline speech recognition (Vosk)** and **natural language processing (OpenAI GPT)**, TasteTreak bridges technology and tradition in a unique and user-friendly way.

---

## 2. 🎯 Objectives

- Create a voice-based UI for native **Telugu-speaking** users.
- Fetch **historical information** about food items using AI.
- Suggest **recipes** based on ingredients users have at home.
- Maintain an intuitive, fast, and offline-first approach using Vosk for voice input.

---

## 3. ⚙️ Technologies Used

| Tool/Library | Purpose |
|--------------|---------|
| **Streamlit** | Web UI framework |
| **Vosk** | Offline Telugu speech recognition |
| **OpenAI API** | Food history via natural language processing |
| **Requests** | API data fetching |
| **Pillow** | Image handling in Streamlit |
| **Pydub** | Audio processing |
| **Python 3.9+** | Core backend scripting |

---

## 4. 🧩 Module Breakdown

### 📁 `app.py`
- Central Streamlit file.
- Sidebar for navigation between "Food History", "Recipe Suggestion", and "About" sections.

### 📁 `history.py`
- Accepts Telugu voice/text input.
- Uses OpenAI to fetch historical or cultural context of dishes.

### 📁 `recipe.py`
- Accepts Telugu voice/text ingredients.
- Fetches or recommends possible recipes.

### 📁 `api_handler.py`
- Contains reusable functions for:
  - Translating speech to text (Vosk).
  - Fetching data from recipe APIs or models.
  - Formatting or parsing inputs.

---

## 5. 🎤 Voice Recognition

- **Model:** `vosk-model-small-te-in-0.42`
- **Language:** Telugu
- **Mode:** Offline — suitable for low-connectivity areas.
- **Usage:** Converts `.wav` audio to text and feeds it to processing modules.

---

## 6. 📚 Data Sources

- **Food history:** Responses generated via OpenAI GPT trained with prompts in Telugu.
- **Recipes:** 
  - Manually curated JSON (for offline demo)
  - Future version: API integration with Indian recipe datasets or scraping from regional sites

---

## 7. 🧪 Testing & Validation

| Test Case | Description | Status |
|-----------|-------------|--------|
| Telugu audio input | Converts to accurate text | ✅ |
| Incorrect input | Shows error message | ✅ |
| Long pauses in speech | Graceful timeout or retry | ✅ |
| Recipe matching | Returns 2–3 matching recipes | ✅ |
| History relevance | Returns 100–150 word description | ✅ |

---

## 8. 📈 Future Enhancements

- Add **text-to-speech (TTS)** for audio output of responses.
- Support for other regional languages (Tamil, Hindi, Kannada).
- Recipe image previews and nutrition info.
- Save and favorite options for user history.
- Deploy on cloud with mobile-first responsive layout.

---

## 9. 🧾 Project Timeline

| Week | Tasks |
|------|-------|
| Week 1 | Streamlit setup, sidebar navigation |
| Week 2 | Vosk integration for Telugu voice input |
| Week 3 | History and recipe modules |
| Week 4 | UI cleanup, testing, and documentation |

---

## 10. 👨‍💻 Team & Contributions

- **Karthik (Developer)**  
  - Streamlit layout & UX  (Tulasi Reddy)
  - Vosk integration and voice flow   (Gowri shankar)
  - GPT-based food history logic  (Chandrika priya)
  - Testing & Documentation

---

## 11. 📌 Conclusion

TasteTreak is more than a food app — it's a **cultural assistant** designed for Telugu speakers. By enabling **regional language support** and
