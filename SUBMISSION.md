# 🏆 Youth Code x AI Hackathon — Submission

## Project Information

**Project Name**: Pudding — AI Cognitive Accessibility Extension  
**Repository**: https://github.com/Tasfia-17/Puddingext  
**Hackathon**: Youth Code x AI — organized by Youth Code Foundation  
**Track**: Track 03 — AI That Actually Helps People

---

## 📋 Quick Links

- **GitHub Repository**: https://github.com/Tasfia-17/Puddingext
- **Demo Guide**: [DEMO_GUIDE.md](DEMO_GUIDE.md)
- **Features Overview**: [FEATURES.md](FEATURES.md)
- **Main README**: [README.md](README.md)

---

## 🎯 What We Built

Pudding is a Chrome browser extension that uses on-device AI (Chrome's built-in Gemini Nano) to adapt web content in real-time for people with dyslexia, ADHD, and cognitive reading challenges — with support for 10 languages.

### The Problem We're Solving

Reading online content is hard for millions of people:
- **8.4 million people with dyslexia** find words jumbling and lines hard to track
- **6.4 million people with ADHD** lose focus in dense text
- **Non-English speakers** face a double barrier — complexity AND language

Existing tools are either privacy-invasive (cloud-based), one-size-fits-all, or English-only.

### Our Solution

Pudding is a **Cognitive Adaptation Engine** that:
1. Learns how *you* read (scroll speed, pauses, rereads)
2. Automatically adapts content difficulty to match your cognitive state
3. Works 100% offline — your data never leaves your device
4. Supports 10 languages, reaching 5+ billion people

---

## 🧠 How AI Powers Pudding

- **Chrome Gemini Nano** — on-device LLM for text simplification, zero privacy risk
- **Cognitive tracker** — behavioral AI that learns your reading patterns locally
- **Complexity analyzer** — NLP-based sentence difficulty scoring
- **Smart auto-mode** — adapts simplification level in real-time based on fatigue signals

---

## 🌍 Track 03 Alignment — AI That Actually Helps People

This project was built specifically for Track 03. It addresses:

- ✅ **Accessibility** — tools for people with dyslexia, ADHD, and cognitive challenges
- ✅ **Neurodiverse individuals** — OpenDyslexic font, focus mode, distraction suppression
- ✅ **Global reach** — 10 languages so the tool works for communities worldwide
- ✅ **Privacy** — 100% offline, no tracking, no data collection

---

## 🛠️ Technical Stack

| Component | Technology |
|-----------|------------|
| Extension framework | Chrome Manifest V3 |
| On-device AI | Chrome Gemini Nano (Prompt API) |
| UI | HTML/CSS/JS |
| Fonts | OpenDyslexic |
| i18n | Custom i18n layer (10 languages) |
| Storage | Chrome local storage (private) |

### Key Files

```
Puddingext/
├── manifest.json           # Chrome extension config
├── content.js              # Page content analysis & transformation
├── popup.js / popup.html   # Extension UI
├── cognitive-tracker.js    # Behavioral reading pattern learning
├── complexity-analyzer.js  # Text difficulty scoring
├── fatigue-detector.js     # Reading fatigue detection
├── focus-mode.js           # Distraction suppression
├── vocabulary-adapter.js   # Vocabulary simplification
├── i18n-helper.js          # 10-language support
└── i18n.json               # Translation strings
```

---

## 💡 Social Value

**Who benefits:**
- Students with dyslexia or ADHD trying to read textbooks and articles
- Non-English speakers navigating English-heavy web content
- Anyone experiencing cognitive fatigue from dense online reading

**Scale of impact:**
- 10 languages → 5+ billion potential users
- 100% private → usable even in sensitive educational/medical contexts
- Works on any webpage → no vendor lock-in

---

## 🎬 Demo Instructions

### Setup

```bash
# Clone repository
git clone https://github.com/Tasfia-17/Puddingext.git

# In Chrome (Dev/Canary):
# chrome://flags/#prompt-api-for-gemini-nano → Enable
# chrome://flags/#optimization-guide-on-device-model → Enable BypassPerfRequirement
# Relaunch Chrome

# Load extension:
# chrome://extensions/ → Developer mode → Load unpacked → select folder
```

### Demo Flow

1. Navigate to any dense article (Wikipedia, news site)
2. Click Pudding icon → select simplification level
3. Hit "Simplify Text" — watch content restructure in real time
4. Enable Focus Mode — distractions disappear
5. Open Complexity Map — see color-coded difficulty heatmap
6. Switch language in the dropdown — UI updates instantly

---

## 📊 Judging Criteria Alignment

| Criterion | How Pudding Qualifies |
|-----------|----------------------|
| **Best Original Idea** | Behavioral AI that *learns* how you read, not static simplification |
| **Best Social Value** | Accessibility for neurodiverse users + 5B+ language reach |
| **Best Presentation** | Full demo guide, SVG diagrams, structured docs |
| **Best UX** | Adaptive, distraction-free, multilingual interface |
| **Best in Category** | Track 03 — purpose-built for helping people with disabilities |

---

## 🚀 What's Next

- [ ] Voice layer with synchronized text highlighting
- [ ] Classroom mode for teachers managing multiple student profiles
- [ ] Study mode with AI-generated flashcards
- [ ] Cross-device profile sync

---

## 🙏 Acknowledgments

- **Youth Code Foundation** for creating this platform
- **Chrome AI Team** for Gemini Nano
- **OpenDyslexic** for the accessibility font
- **Accessibility community** for the inspiration

---

**Built with care for the people who need it most.** 🍮
