# 💬 WhatsApp Chat Analyzer

A lightweight, zero-dependency Java CLI tool that parses exported WhatsApp chat logs (`_chat.txt`) to extract fun message analytics—such as who says "I love you" most frequently and who initiates sentiment after long pauses.

Built as a weekend project to practice modern Java syntax (Records, Streams API, `java.time`, and File I/O).

---

## 🚀 Features

- **File Parser:** Reads standard WhatsApp export text files line-by-line using Regex and Java NIO.
- **Frequency Stats:** Tracks total count of specific words/phrases per user using the Java Streams API.
- **Initiator Tracking:** Detects who says targeted phrases _first_ after conversation pauses (e.g., > 6 hours).
- **Zero Dependencies:** Uses only standard Java 17+ libraries (`java.nio`, `java.time`, `java.util`).

---

## 🛠️ Requirements

- **Java Development Kit (JDK) 17** or higher.

---

## 📖 How to Export Your WhatsApp Chat

1. Open a chat in WhatsApp on your phone.
2. Tap **Settings / More Options** (three dots) > **More** > **Export Chat**.
3. Select **Without Media**.
4. Save the generated `.txt` file as `_chat.txt` in your project folder.

---

## 🏃 Getting Started

### 1. Compile the Project

```bash
javac App.java
```

### 2. Run the Project

```bash
java App _chat.txt
```

### 3. Example Output

==========================================
WHATSAPP CHAT ANALYTICS  
==========================================
Total Messages Parsed: 14,352

--- "Love You" Frequency ---
• Sam : 412 times
• Alex : 298 times

--- First to Say "Love You" (6h+ Gap) ---
• Sam : 84 times (Initiator Champ)
• Alex : 31 times
==========================================
