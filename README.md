# Speak Academy Grammar Games

A collection of interactive HTML5 games for ESL (English as a Second Language) learning. All games are mobile-friendly, work offline, and load content from JSON files for easy customization.

🔗 **Live Demo:** https://speakacademyes.github.io/grammar_games/

---

## 🎮 Available Games

| Game | Description | Best For |
|------|-------------|----------|
| **Anagram** | Unscramble letters to spell words | Vocabulary, Spelling |
| **Spin the Wheel** | Random selection spinner | Speaking prompts, Topic selection |
| **Open the Box** | Tap numbered boxes to reveal content | Vocabulary reveal, Surprises |
| **Unjumble** | Reorder words to form sentences | Sentence structure, Grammar |
| **Matching Pairs** | Memory game with EN/ES word pairs | Vocabulary, Translation |
| **Group Sort** | Drag items into correct categories | Classification, Vocabulary groups |
| **Speaking Cards** | Draw cards with conversation prompts | Speaking practice, Discussion |
| **Find the Match** | Tap the matching answer from options | Quick recall, Vocabulary |
| **Label the Diagram** | Tap hotspots on an image | Visual vocabulary, Body parts, Objects |

---

## 📁 File Structure

```
grammar_games/
├── index.html              # (optional) Game menu/launcher
├── anagram-game.html
├── spin-the-wheel.html
├── open-the-box.html
├── unjumble.html
├── matching-pairs.html
├── group-sort.html
├── speaking-cards.html
├── find-the-match.html
├── label-diagram.html
├── hotspot-editor.html     # Tool for creating label-diagram activities
│
└── words/                  # JSON content files
    ├── weather-disasters.json
    ├── wheel-items.json
    ├── box-items.json
    ├── unjumble-sentences.json
    ├── matching-pairs.json
    ├── group-sort.json
    ├── speaking-cards.json
    ├── find-match.json
    └── label-diagram.json
```

---

## 🚀 Quick Start

### 1. Basic Usage
Simply open any game HTML file in a browser. Games include fallback content if no JSON is loaded.

### 2. Load Custom Content
Add a `?set=` parameter to load different JSON files:

```
anagram-game.html?set=irregular-verbs
spin-the-wheel.html?set=grammar-topics
matching-pairs.html?set=food-vocabulary
```

This loads `words/irregular-verbs.json`, `words/grammar-topics.json`, etc.

### 3. Load from External URL
You can also load JSON from any URL:

```
anagram-game.html?set=https://example.com/my-words.json
```

---

## 📝 JSON Formats

### Anagram Game
Words or short phrases to unscramble.

```json
{
  "title": "Weather & Natural Disasters",
  "words": [
    "tsunami",
    "earthquake",
    "hurricane",
    "thunderstorm"
  ]
}
```

---

### Spin the Wheel
Items to randomly select from.

```json
{
  "title": "Grammar Topics",
  "items": [
    "Present Simple",
    "Past Continuous",
    "Present Perfect",
    "Conditionals"
  ]
}
```

---

### Open the Box
Items hidden inside numbered boxes.

```json
{
  "title": "Classroom Objects",
  "items": [
    "Pencil ✏️",
    "Notebook 📓",
    "Ruler 📏",
    "Scissors ✂️"
  ]
}
```

---

### Unjumble
Complete sentences to reorder.

```json
{
  "title": "Basic Sentences",
  "sentences": [
    "I am learning English.",
    "She goes to school every day.",
    "They are playing in the park.",
    "Do you like chocolate ice cream?"
  ]
}
```

---

### Matching Pairs
English-Spanish (or any language pair) vocabulary.

```json
{
  "title": "Basic Vocabulary (EN-ES)",
  "pairs": [
    { "english": "House", "spanish": "Casa" },
    { "english": "Dog", "spanish": "Perro" },
    { "english": "Water", "spanish": "Agua" },
    { "english": "Book", "spanish": "Libro" }
  ]
}
```

---

### Group Sort
Items to categorize into groups.

```json
{
  "title": "Food Categories",
  "groups": [
    {
      "name": "Fruits",
      "items": ["Apple", "Banana", "Orange", "Grape"]
    },
    {
      "name": "Vegetables",
      "items": ["Carrot", "Broccoli", "Potato", "Onion"]
    },
    {
      "name": "Dairy",
      "items": ["Milk", "Cheese", "Yogurt", "Butter"]
    }
  ]
}
```

---

### Speaking Cards
Prompts for conversation practice.

```json
{
  "title": "Conversation Starters",
  "category": "Question",
  "cards": [
    "What did you do last weekend?",
    "Describe your favorite place to visit.",
    "What would you do with a million dollars?",
    "Tell me about your best friend."
  ]
}
```

---

### Find the Match
Prompt-answer pairs for quick matching.

```json
{
  "title": "English - Spanish Basics",
  "pairs": [
    { "prompt": "Hello", "answer": "Hola" },
    { "prompt": "Goodbye", "answer": "Adiós" },
    { "prompt": "Thank you", "answer": "Gracias" },
    { "prompt": "Please", "answer": "Por favor" }
  ]
}
```

---

### Label the Diagram
Image with hotspot coordinates (x, y as percentages).

```json
{
  "title": "Body Parts",
  "image": "images/body.png",
  "hotspots": [
    { "label": "Head", "x": 50, "y": 8 },
    { "label": "Shoulder", "x": 32, "y": 22 },
    { "label": "Elbow", "x": 20, "y": 45 },
    { "label": "Knee", "x": 40, "y": 70 }
  ]
}
```

> 💡 **Tip:** Use the **Hotspot Editor** tool (`hotspot-editor.html`) to visually create these coordinates!

---

## 🛠️ Hotspot Editor Tool

The **Hotspot Editor** makes it easy to create Label the Diagram activities:

1. Open `hotspot-editor.html`
2. Upload an image or paste a URL
3. Click on the image to place hotspots
4. Enter a label for each hotspot
5. Click **Export JSON** to download the file

---

## 🎯 Game Features

All games include:

| Feature | Description |
|---------|-------------|
| ❤️ **Lives** | 3 lives (where applicable) |
| ⭐ **Score** | Points for correct answers |
| 🔥 **Streak** | Bonus for consecutive correct answers |
| 📊 **Progress Bar** | Visual progress tracking |
| 🔊 **Sound Effects** | Audio feedback (with mute toggle) |
| 📱 **Mobile Friendly** | Touch-optimized, responsive design |
| 🎨 **Speak Academy Branding** | Consistent black/orange/white theme |

### Gamification Elements

- **Stars (⭐⭐⭐):** Earned based on hints used (3 = no hints, 2 = 1 hint, 1 = 2+ hints)
- **Lifelines:** Hint, Reveal Vowels, Skip (where applicable)
- **Streak Bonus:** Extra points for consecutive correct answers
- **Accuracy %:** Shown at game completion

---

## 🎨 Customization

### Colors
Games use CSS custom properties. Edit the `:root` section in any game:

```css
:root {
  --black: #1a1a1a;
  --orange: #ff6b35;
  --white: #ffffff;
  --success: #4caf50;
  --danger: #ef4444;
}
```

### Fonts
Games use Google Fonts:
- **Outfit** — UI text
- **JetBrains Mono** — Game content, scores

---

## 📱 Deployment

### GitHub Pages
1. Push all files to a GitHub repository
2. Go to Settings → Pages
3. Select branch (main) and folder (root)
4. Access at `https://username.github.io/repository-name/`

### Any Web Server
Simply upload all HTML files and the `words/` folder to your web server.

### Offline Use
Games work offline once loaded. For true offline use, download all files locally.

---

## 💡 Tips for Teachers

1. **Create topic-specific JSON files** for each lesson
2. **Use URL parameters** to quickly switch between word sets
3. **Bookmark specific game+content combinations** for easy access
4. **Use the Hotspot Editor** to create visual vocabulary activities
5. **Combine games** — e.g., Spin the Wheel to select topics, then Anagram for practice

---

## 📄 License

Free for educational use. Created for Speak Academy.

---

## 🤝 Contributing

To add new content:
1. Create a JSON file following the format above
2. Place it in the `words/` folder
3. Access via `?set=your-filename` (without .json)

To report issues or suggest features, contact Speak Academy.
