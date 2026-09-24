# 💬 Sentiment Analytics & Dual-Chat Web App

A lightweight, real-time sentiment analysis web application designed to evaluate dual-participant text conversations using a customized **VADER Sentiment Analysis engine** built natively in JavaScript.

🚀 **Live Demo:** [https://srshriram-01.github.io/sentiment_analyzer/](https://srshriram-01.github.io/sentiment_analyzer/)

---

## ✨ Features

* **Real-Time Sentiment Scoring:** Evaluates text input instantly and calculates compound scores ranging from `-1.0` (Highly Negative) to `+1.0` (Highly Positive).
* **Gen Z & Modern Slang Vocabulary:** Custom-built dictionary extensions incorporating modern internet lingo, abbreviations, and context swaps (e.g., *cooked*, *cooking*, *slay*, *mid*,*fr*, *no cap*).
* **Dual-Participant Simulation:** Alternate between Person 1 and Person 2 to simulate real-time chat interactions.
* **Frequency Analytics:** Automatically tracks and displays most used words and emojis for both participants individually and combined.
* **Transcript & Stats Export:** Generates downloadable text transcripts along with summary statistics.
* **Zero Backend Required:** Runs entirely in the client browser using vanilla HTML5, CSS3, and JavaScript.

---

## 🛠️ How It Works

The core analyzer uses an adapted **VADER (Valence Aware Dictionary and sEntiment Reasoner)** rule-based model:

1. **Preprocessing:** Text is tokenized, stripped of punctuation, and normalized for casing.
2. **Context Matching:** Phrases like *"got cooked"* or *"let him cook"* map directly to contextual sentiment values before single-word lookup.
3. **Lexicon Scoring:** Words are matched against the VADER dictionary (including custom slang weights).
4. **Normalization:** Individual raw word scores ($x$) are normalized into a final compound score using the VADER formula:

$$\text{Compound Score} = \frac{x}{\sqrt{x^2 + 15}}$$

---

## 🚀 Quick Start (Local Setup)

No dependencies or node packages required!

1. Clone or download this repository:
   ```bash
   git clone [https://github.com/srshriram-01/sentiment_analyzer.git](https://github.com/srshriram-01/sentiment_analyzer.git)
