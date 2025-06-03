# 🏺 Egyptian Artifact Chatbot — Phase Project

This project scrapes real-world artifact data from the [Global Egyptian Museum](https://www.globalegyptianmuseum.org), using NLP, analyzes image similarity, and wraps it all into a chatbot interface for inquiry.

Not just a bot but a dataset builder, annotator, and a side quest into image understanding. Built this from scratch to explore what it takes to go from raw data scraping to a usable conversational assistant.

---

## Project Structure

### **Phase 1–2: Data Collection**
- Scraped detailed artifact data and images from the Global Egyptian Museum website.
- Used `BeautifulSoup` to extract titles, descriptions, technical metadata, and image links.
- Downloaded images and saved all metadata in structured `JSON`.

### **Phase 3: NLP Enhancement**
- Used spaCy (`en_core_web_sm`) to extract and embed named entities into artifact descriptions.
- Output: `artifacts_FinalData.json` with both original and enhanced descriptions.

### **Phase 4: **
- Basic duplicate removal on artifact entries by title.

### **Phase 5: Image Similarity**
- Used OpenCV to compute color histograms for all artifact images.
- Compared images using Bhattacharyya distance to find visually similar artifacts.
- Saved top similar image results to a separate folder for any input image.
- In the demo i created two image similarity code

### **Phase 6: Chatbot**
- Simple text-based CLI chatbot interface (no UI yet).
- Searches artifacts using keyword match on titles and descriptions.
- Outputs core metadata and historical context.
- Meant for testing interaction flow and information delivery.



---


##  To Run

### 1. Install dependencies:
```bash
pip install requests beautifulsoup4 spacy opencv-python numpy matplotlib
python -m spacy download en_core_web_sm
```



---

## Notes

- Site scraping logic is specific to how `globalegyptianmuseum.org` structures its HTML — if that changes, this breaks.
- Only basic NLP done here; no deep contextual rewriting.
- Chatbot works off keywords — no semantic search yet.

---

## My Goal for this project

Wanted to build something tangible to build a simple bot and create a project about connecting with real cultural data, seeing how far Python alone can go in making static artifacts interactive.

---

