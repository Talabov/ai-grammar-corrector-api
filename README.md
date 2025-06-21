
# AI-Powered Grammar Corrector API

A clean and production-ready Flask API that automatically fixes grammar issues in English text using a pretrained T5 model from HuggingFace.

---

## ✅ Key Features

- 📦 Flask-based RESTful API
- 🤖 Uses `vennify/t5-base-grammar-correction` model
- 🛡 Input validation & error handling
- 🚦 Built-in rate limiting: 10 requests/minute
- ⚙️ JSON input/output structure
- 🔁 Automatic model download on first run
- 🧪 Tested with Postman — 100% working

---

## 🚀 Endpoint

**POST** `/correct`

### Example Request:
```json
{
  "text": "he go to school every day"
}
```

### Example Response:
```json
{
  "corrected": "He goes to school every day."
}
```

---

## ⛔ Rate Limiting

The API is rate-limited to **10 requests per minute** per IP address.  
Exceeding this limit will return:

```json
{
  "error": "Rate limit exceeded. Please try again later."
}
```

---

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```

This includes:
- Flask
- Flask-CORS
- Flask-Limiter
- Transformers
- Torch
- Python-Dotenv

---

## 🖥 How to Run

```bash
python "AI-Powered Grammar Corrector API.py"
```

Server will start at:
```
http://127.0.0.1:5000/correct
```

---

## 🧪 Screenshots (From Postman)

- ✅ Successful correction (200 OK)
- ⚠️ Empty input → 400 error
- 🔁 Exceeded limit → 429 error
- 🖥 Console log with model loading and request logs

> 💡 You can see real examples on the Gumroad gallery.

---

## 💼 Ready-to-Use Version

You can get a ZIP version with all files, setup instructions, `.env.example`, and more:

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

## 📬 Need this functionality in another language or stack (e.g. Node.js, Go, etc)?

Contact the author: talabov.ali72@gmail.com  
📬 Telegram: [@talabovali](https://t.me/talabovali)  
💡 **Note:** Pricing may vary depending on complexity and target stack.
