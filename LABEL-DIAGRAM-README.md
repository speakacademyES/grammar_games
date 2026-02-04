# Label the Diagram

An interactive game where students tap hotspots on an image to identify labeled parts. Perfect for teaching vocabulary like body parts, classroom objects, maps, and more.

---

## 🎮 Two Modes

### 👨‍🏫 Teacher Mode (Default)
Open the game without any URL parameters to enter Teacher Mode:
```
label-diagram.html
```

**What you see:**
- Drag & drop zone for JSON files
- Drop your JSON → game starts immediately
- Great for live classroom sessions

---

### 👨‍🎓 Student Mode (Practice)
Add `?set=` parameter to go directly to gameplay:
```
label-diagram.html?set=body-parts
```

**What students see:**
- Game loads immediately (no startup screen)
- No editing options
- Clean interface for practice

---

## 🚀 Quick Start

### For Live Classroom Use

1. Open `label-diagram.html` in your browser
2. Drag & drop your JSON file onto the startup screen
3. Game starts automatically
4. Play with your students!

### For Homework/Practice

1. Create your JSON using the **Hotspot Editor** (see below)
2. Save the file (e.g., `kitchen-items.json`)
3. Upload to your `words/` folder on GitHub:
   ```
   grammar_games/
   └── words/
       └── kitchen-items.json
   ```
4. Share this link with students:
   ```
   https://speakacademyes.github.io/grammar_games/label-diagram.html?set=kitchen-items
   ```

---

## 🛠️ Creating Content with Hotspot Editor

The **Hotspot Editor** (`hotspot-editor.html`) lets you visually create activities:

### Step-by-Step

1. **Open** `hotspot-editor.html`

2. **Add an image:**
   - Drag & drop an image file, OR
   - Paste an image URL

3. **Place hotspots:**
   - Click anywhere on the image
   - Enter the label (e.g., "Elbow")
   - Repeat for all parts

4. **Set the title:**
   - Enter a title like "Body Parts" or "Kitchen Items"

5. **Export:**
   - Click **Export JSON** to download the file
   - Or click **Copy JSON** to copy to clipboard

6. **Use it:**
   - **In class:** Drag the JSON into `label-diagram.html`
   - **For homework:** Upload to `words/` folder and share the link

---

## 📝 JSON Format

```json
{
  "title": "Body Parts",
  "image": "images/body.png",
  "hotspots": [
    { "label": "Head", "x": 50, "y": 8 },
    { "label": "Shoulder", "x": 32, "y": 22 },
    { "label": "Elbow", "x": 20, "y": 45 },
    { "label": "Knee", "x": 40, "y": 70 },
    { "label": "Foot", "x": 42, "y": 95 }
  ]
}
```

| Field | Description |
|-------|-------------|
| `title` | Activity name (shown at top of game) |
| `image` | Path to image or full URL |
| `hotspots` | Array of labels with x/y coordinates |
| `x`, `y` | Position as percentage (0-100) from top-left |

---

## 🖼️ Image Tips

### Option 1: Use a URL
```json
"image": "https://example.com/my-image.png"
```
- Works immediately
- No upload needed
- Image must be publicly accessible

### Option 2: Host your own images
```json
"image": "images/body.png"
```
- Create an `images/` folder in your GitHub repo
- Upload your images there
- Reference them with relative paths

### Recommended Image Specs
- **Format:** PNG or JPG
- **Size:** 500-800px wide
- **Background:** Clean, simple backgrounds work best
- **Orientation:** Portrait or landscape both work

---

## 🎯 Game Features

| Feature | Description |
|---------|-------------|
| ❤️ **3 Lives** | Lose one for each wrong tap |
| ⭐ **Score** | 10+ points per correct answer |
| 🔥 **Streak** | Bonus points for consecutive correct answers |
| 📊 **Progress** | Visual bar showing completion |
| 📈 **Accuracy** | Shown at end of game |
| 🔊 **Sound** | Audio feedback (can be muted) |
| 📱 **Mobile** | Touch-friendly, responsive design |

---

## 📁 File Structure

```
grammar_games/
├── label-diagram.html      # The game
├── hotspot-editor.html     # Tool to create activities
│
├── images/                 # Your custom images (optional)
│   ├── body.png
│   └── kitchen.png
│
└── words/                  # JSON content files
    ├── body-parts.json
    ├── kitchen-items.json
    └── classroom-objects.json
```

---

## 🔗 URL Reference

| URL | Mode | Use Case |
|-----|------|----------|
| `label-diagram.html` | Teacher | Drag & drop JSON for live class |
| `label-diagram.html?set=body-parts` | Student | Direct link to specific activity |
| `hotspot-editor.html` | — | Create new activities |

---

## 💡 Activity Ideas

| Topic | Image Suggestion |
|-------|------------------|
| Body Parts | Human body diagram |
| Face | Close-up face diagram |
| Classroom | Photo of classroom |
| Kitchen | Kitchen scene |
| Living Room | Room layout |
| City/Map | Simple map |
| Animals | Animal diagram |
| Bicycle/Car | Vehicle parts |
| Computer | Desktop setup |
| Food/Plate | Meal with labeled items |

---

## ❓ Troubleshooting

### "Could not load image"
- Check the image URL is correct and publicly accessible
- If using local files, make sure the path is relative to the HTML file

### Hotspots in wrong position
- Coordinates are percentages (0-100), not pixels
- Use the Hotspot Editor to place them visually

### Students see the startup screen
- Make sure the URL includes `?set=filename`
- Check the JSON file exists in the `words/` folder
- Filename is case-sensitive

---

## 📄 Example Files

### Sample JSON: `body-parts.json`
```json
{
  "title": "Body Parts",
  "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Human_body_features_en.svg/500px-Human_body_features_en.svg.png",
  "hotspots": [
    { "label": "Head", "x": 50, "y": 8 },
    { "label": "Shoulder", "x": 32, "y": 22 },
    { "label": "Chest", "x": 50, "y": 28 },
    { "label": "Arm", "x": 22, "y": 38 },
    { "label": "Hand", "x": 18, "y": 55 },
    { "label": "Leg", "x": 40, "y": 70 },
    { "label": "Knee", "x": 42, "y": 78 },
    { "label": "Foot", "x": 42, "y": 95 }
  ]
}
```

---

Created for **Speak Academy** 🎓
