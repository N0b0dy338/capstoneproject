# AllergyAware

A client-side web app suite for people managing food allergies. No backend, no installation — open in a browser and go.

## Tools

### Food Label Translator (`translator.html`)
Scan or photograph a food label and get an instant allergen report in your language.

1. Capture a photo with your camera or upload an image
2. Optionally drag to select just the ingredients area
3. Run OCR (powered by Tesseract.js) to extract the ingredient text
4. Select a language — the app detects which of the 14 EU allergens are present and translates both the allergen names and the full ingredient list via the MyMemory API

### Allergy Card Creator (`allergy-card.html`)
Build a personalised allergy card to show at restaurants when travelling abroad.

1. Check off which allergens you have
2. Select up to 3 languages
3. Generate a card that states you have a life-threatening allergy to your selected items and asks whether the food is safe — shown in the target language with English alongside for reference
4. Print the card directly from the browser

## Running locally

Serve the project root with any static file server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`. A local server is required (rather than opening files directly) because the camera API needs a secure context.

## Dependencies

All dependencies are loaded from CDN — no `npm install` needed.

- [Tesseract.js v5](https://github.com/naptha/tesseract.js) — in-browser OCR
- [MyMemory Translation API](https://mymemory.translated.net) — free, no API key required
