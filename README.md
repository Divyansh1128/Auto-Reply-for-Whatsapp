
# 🤖 WhatsApp Web Auto-Replier

An automated responder for WhatsApp Web built with Python. It simulates user actions to read and respond to incoming messages using OpenAI's language models (via API), enabling real-time chat automation.

## 📦 Features

- Automatically detects new messages on WhatsApp Web
- Reads the incoming message using clipboard functionality
- Generates smart replies using OpenAI's GPT
- Sends replies back using simulated keyboard and mouse actions
- Simple and lightweight — no browser automation or Selenium required

## 🔧 Requirements

Install the required libraries before running the script:

```bash
pip install pyautogui pyperclip openai
```

> `time` is part of Python’s standard library.

## 🧠 Tech Stack

- `pyautogui`: Simulates mouse and keyboard input
- `pyperclip`: Handles clipboard copy-paste operations
- `time`: Adds delays for synchronization
- `openai`: Sends message context to the GPT model and fetches responses

## 🛠 Setup

1. **Get your OpenAI API key**  
   Sign up at [platform.openai.com](https://platform.openai.com) and generate your secret API key.

2. **Add the API key to your script**  
   In your Python script:

   ```python
   from openai import OpenAI

   client = OpenAI(
       api_key="your-api-key-here"
   )
   ```

3. **Open WhatsApp Web**  
   - Go to [https://web.whatsapp.com](https://web.whatsapp.com)
   - Log in by scanning the QR code with your phone
   - Keep the tab active and visible for the script to work correctly

4. **Run the Python script**  
   Run the script in your terminal or IDE:

   ```bash
   python auto_replier.py
   ```

## ⚠️ Notes

- Make sure WhatsApp Web is visible on the screen — this script depends on screen coordinates and image recognition.
- You might need to calibrate click positions or delays based on your screen resolution.
- Use responsibly. Spamming or misuse may violate WhatsApp's terms of service.

## 📄 Example

```python
import pyautogui
import pyperclip
import time
from openai import OpenAI

client = OpenAI(api_key="your-api-key")

while True:
    # logic to locate new message, click, copy text
    # get text and send to OpenAI
    # generate response and type it back
    time.sleep(2)
```

## 🧑‍💻 Author

**Divyansh Raj**

## 📃 License

This project is licensed under the MIT License.
